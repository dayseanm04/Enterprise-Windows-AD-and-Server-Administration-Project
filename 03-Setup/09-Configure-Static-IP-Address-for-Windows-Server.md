# 09 - Configure Static IP Address for thd Windows 2019 Server

## Overview

I will configure a **static IP address** for the **Windows Server 2019 virtual machine**.  

Assigning a static IP is critical for servers, especially **Domain Controllers**, because network services such as:
- Active Directory
- DNS
- Authentication

This server will function as the **Domain Controller** for the Oak Town Corporate Services environment.

---

# Server Information

**Server VM Name:** Windows-2019-SRV <br/>
**Server name (computer name):** OTCS-SRV-DC01 <br/>
**Role:** Domain Controller <br/>
**Network Type:** Static IP Configuration <br/>

---

# Verify Current IP Address (DHCP)

Before configuring a static IP, I verified the current network configuration.

### Step 1

Open **Command Prompt**.

### Step 2

Run the following command:

```bash
ipconfig /all
```

### Result

<img width="900" height="485" alt="30" src="https://github.com/user-attachments/assets/090da12a-623b-4f56-ac22-9e5e206beb86" />


Note: This IP is the IP this Server first received when I configured this VM using the default switch.
















