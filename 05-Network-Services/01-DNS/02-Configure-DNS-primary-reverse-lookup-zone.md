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

---

## Step-by-Step Configuration

### Step 1: Open DNS Manager
1. Launch **Server Manager** on the domain controller.
2. Click on the **Tools** menu located in the top-right navigation bar.
3. Select **DNS** from the drop-down options to open the management console.

<img width="391" height="208" alt="1" src="https://github.com/user-attachments/assets/781e6a6b-f35f-4830-86ea-6149fa0ea643" />

### Step 2: Launch the New Zone Wizard
1. In the **DNS Manager** console tree, look under your server node (`OTCS-DC01.corp.oaktowncs`).
2. Locate and right-click on the folder named **Reverse Lookup Zones**.
3. Click on **New Zone...** from the contextual menu.

