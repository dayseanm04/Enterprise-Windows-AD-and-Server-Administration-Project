# 01 – Troubleshoot and Resolve Domain Controller Internet Connectivity Issue

## Overview

During the configuration of the Windows Server 2019 Domain Controller (**OTCS-SRV-DC01**), the server was unable to access the internet.

This issue prevented access to external resources such as websites.

This document outlines the troubleshooting process, root cause, and resolution.

Note: Windows-2019-SRV VM is the OTCS-SRV-DC01

---

# Problem

The Domain Controller(**OTCS-SRV-DC01**) could not access the internet.

### Symptoms:

<img width="713" height="502" alt="TS1" src="https://github.com/user-attachments/assets/a14bbf93-95b5-4dea-9b00-21ac2b8f2906" />

I searched for youtube on Google Chrome (on the Production server(**OTCS-SRV-DC01**)
- Site couldnt be reached
- DNS address could not be found

1. The Windows-2019-SRV VM is connected to OTCS-SW (a virtual switch [Hyper-V external]).
<img width="256" height="132" alt="TS2" src="https://github.com/user-attachments/assets/e307dcfb-0a4d-4f43-ab3d-559b28225a9d" />

2. Clicked on the Ethernet Logo at the bottom right (note the triangle exclamation sign [warning sign])
<img width="367" height="221" alt="TS3" src="https://github.com/user-attachments/assets/a3220c38-846d-4418-abc4-7e65c85bfbc1" />

<img width="573" height="359" alt="TS4" src="https://github.com/user-attachments/assets/92c52325-2e88-44fc-9667-b1355e1c0308" />

---

## Initial Investigation

### Step 1 – Verify Network Connection

- Confirmed the server was connected to OTCS-SW (External Virtual Switch)

<img width="725" height="359" alt="TS5" src="https://github.com/user-attachments/assets/2e7a817c-4631-47ee-bdf8-f25bd3ec9347" />

### Step 2 – Check IP Configuration

Ran the following command in command prompt or PowerShell:

```cmd
ipconfig /all
```

<img width="856" height="522" alt="TS6" src="https://github.com/user-attachments/assets/ef90572d-59fb-4015-a1ae-83637d7df589" />

Note: This DNS server is my loopback IP address

### Step 3 – Check DNS Configuration

1. Open Server Manager

<img width="596" height="174" alt="TS7" src="https://github.com/user-attachments/assets/7c46ed2c-9cf2-4c6b-8a12-3005c87d49be" />

2. Click on Tools, then click on DNS

<img width="599" height="509" alt="TS8" src="https://github.com/user-attachments/assets/355c7a92-f1f1-4f35-b1db-0c0367dcb8d5" />

Note: Under Interfaces all of the IP addresses listed are the Server IP addresses.
Click on **Fowarders**

<img width="686" height="495" alt="TS9" src="https://github.com/user-attachments/assets/bb17c52b-0e8f-4434-bf71-f6316f2871ad" />

Note: this IP is the IP address the Server first received when I configured the VM using the default switch.










