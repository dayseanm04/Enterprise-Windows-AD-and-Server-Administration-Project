# 09 -Configure Static IP Address for thd Windows 2019 Server

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

Note: This IP is the IP this Server first received when I configured this VM using the default switch.
