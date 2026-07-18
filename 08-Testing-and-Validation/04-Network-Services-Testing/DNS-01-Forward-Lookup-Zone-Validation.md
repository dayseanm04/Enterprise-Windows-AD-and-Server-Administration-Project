# 01 - DNS Forward Lookup Validation

## Overview
In this task I will demonstrate how to test and validate the functionality of the DNS Forward Lookup Zone using ping commands on both the domain controller and a remote Windows 11 host.

---

## Objectives
- Perform local forward lookup testing on the domain controller.
- Validate local IPv4 forward lookup resolution on the domain controller.
- Validate remote client-side name resolution and network connectivity from a Windows 11 host.

---

## Environment
- **Domain Controller:** **OTCS-DC01** (IP: **`192.168.1.2`**, Loopback: **`127.0.0.1`** / **`::1`**)
- **Client Machine:** Windows 11 Host (IP: **`192.168.1.3`**)
- **Configured Domain:** corp.oaktowncs.com
- **Tools Used:** 
  - Windows Command Prompt (CMD)
  - Windows PowerShell

---

## Method 1: Local Server-Side Validation

### Pre-Configuration Note
When I configured a static IP for the domain controller OTCS-DC01 I configured the primary DNS server to itself 127.0.0.1

### Steps
1. Logged into the domain controller **OTCS-DC01** as Administrator.
2. Open **Command Prompt** as an Administrator.
3. Execute a default ping command to test native resolution:

```cmd
ping otcs-dc01
ping -4 otcs-dc01 (this shows the IPv4 address)
```

<img width="751" height="453" alt="1" src="https://github.com/user-attachments/assets/b28c141f-4976-4d20-9295-94a063e88c82" />

## Method 2: Remote Client-Side Validation

### Pre-Configuration Note
Now I will test the dns using my host machine (win 11 [192.168.1.3])
I've set the DNS server to the windows server(OTCS-DC01 [192.168.1.2])

### Steps

1. Log into the external client machine (Windows 11 Host).
2. Open Windows PowerShell.
3. Execute a forward lookup connectivity test against the target domain controller hostname:

<img width="752" height="303" alt="2" src="https://github.com/user-attachments/assets/062e8e2c-d3f8-400e-b850-130873344b21" />


