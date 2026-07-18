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

