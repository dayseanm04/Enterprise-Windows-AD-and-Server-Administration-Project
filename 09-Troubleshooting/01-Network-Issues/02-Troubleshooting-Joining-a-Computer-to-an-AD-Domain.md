# Troubleshooting: Joining a Computer to a Domain

##  Summary
* **Problem:** Failed to join the Windows 11 host machine (`comp-a-test`) to the Active Directory domain `corp.oaktowncs.com`.
* **Environment:** 
  * **Domain Controller / DNS Server:** `OTCS-DC01` running Windows Server 2019 on a Hyper-V VM (`192.168.1.2`).
  * **Client Machine:** Windows 11 Host Machine (`192.168.1.3`) connected via `vEthernet (OTCS-SW)`.

---

## Problem 1: Active Directory Domain Controller Could Not Be Contact

### What I Seen
* When attempting to join the domain via System Properties, an error dialog displays: *"An Active Directory Domain Controller (AD DC) for the domain 'corp.oaktowncs.com' could not be contacted."*
* Clicked details shows: `The error was: "DNS name does not exist." (error code 0x0000232B RCODE_NAME_ERROR)`.
* The network query failed to find the service location (SRV) record for `_ldap._tcp.dc._msdcs.corp.oaktowncs.com`.

<img width="800" height="424" alt="1" src="https://github.com/user-attachments/assets/eb5b9b15-33bb-4504-8623-99dcb642e5e2" />

### Analysis
* I havent configured the host computer `comp-a-test` to use the Windows Server as its DNS server. Because it was using my ISP DNS, it could not resolve the internal private Active Directory domain name or locate the Domain Controller.

### What I Did
1. Opened **Control Panel**, Click **Network and Sharing Center** on the host machine.
2. Clicked on the network connection **vEthernet (OTCS-SW)** and opened **Properties**.
3. Selected **Internet Protocol Version 4 (TCP/IPv4)** and clicked **Properties**.
4. Selected "Use the following IP address" and "Use the following DNS server addresses" and configured:
  
<img width="395" height="452" alt="0" src="https://github.com/user-attachments/assets/f684a6a3-194f-4042-8e37-7b7eb83d3ad9" />

5. Opened PowerShell and ran `ipconfig /all` to verify that the host machine's DNS Server was correctly set to `192.168.1.2`.

<img width="856" height="378" alt="1" src="https://github.com/user-attachments/assets/df3fd463-64a3-4cc6-86a1-bf9c8615dda2" />

---

## Problem 2: General Network Error validating the Computer Name

### What I See
* After fixing the DNS settings on the client, a second domain join attempt failed with a new error message: *"The following error occurred validating the name 'COMP-A-TEST'. A general network error occurred."*

### Analysis
* Network reachability was confirmed using bi-directional ping tests:
  * Pinged the server from the host machine (`ping 192.168.1.2`) **Success**.
  * Pinged the host from the server VM (`ping 192.168.1.3`) **Success**.
  * Pinged the domain name from the host machine (`ping -4 corp.oaktowncs.com`)  **Success** (Resolves to `192.168.1.2`).

<img width="780" height="319" alt="2" src="https://github.com/user-attachments/assets/755f8b19-9387-48f0-8041-fca21a01dfc3" />
<img width="629" height="230" alt="3" src="https://github.com/user-attachments/assets/89aa271e-b32d-40b4-a2c3-3446cac7a159" />
<img width="714" height="284" alt="4" src="https://github.com/user-attachments/assets/133c7f11-a0d5-4d56-9a74-9f99adb3dd8b" />

### What I Did
1. Switched to the Windows Server VM (`OTCS-DC01`).
2. I then configure a **New Host (A or AAAA)** for **comp-a-test**
3. I check the box to **Create associated pointer (PTR) record


