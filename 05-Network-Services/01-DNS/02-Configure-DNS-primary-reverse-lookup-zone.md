# Configure an Active Directory-Integrated Reverse Lookup Zone

## Overview

In this task I will configure an Active Directory-Integrated Primary Reverse Lookup Zone in Windows Server. A Reverse Lookup Zone performs the opposite function of a forward lookup zone by resolving known network IP addresses back into human-readable hostnames (such as translating `192.168.1.2` back into `OTCS-DC01.corp.oaktowncs.com`). 

---

## Objectives
- Configure a Primary Reverse Lookup Zone integrated directly into Active Directory.

---

## Environment
- **Domain Controller:** OTCS-DC01 (`OTCS-DC01.corp.oaktowncs`)
- **Target Subnet Network ID:** `192.168.1.0/24`
- **Domain Namespace:** corp.oaktowncs.com
- **Tools Used:** 
  - Server Manager
  - DNS Manager Console
