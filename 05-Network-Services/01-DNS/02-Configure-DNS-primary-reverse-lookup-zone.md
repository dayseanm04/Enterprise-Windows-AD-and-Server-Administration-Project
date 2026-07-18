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

<img width="756" height="282" alt="2" src="https://github.com/user-attachments/assets/6033f023-04b8-4e8f-8def-c46ea8764cf2" />

4. When the **New Zone Wizard** welcome window initializes, click **Next**.

### Step 3: Select Zone Type and Active Directory Integration
1. On the **Zone Type** parameters screen, select the **Primary zone**. 
2. Check the box at the bottom labeled **Store the zone in Active Directory (available only if DNS server is a writeable domain controller)**.
3. Click **Next**.

<img width="650" height="426" alt="3" src="https://github.com/user-attachments/assets/1a9d1ca3-5afd-4b01-9149-3468381fdb18" />

### Step 4: Choose the Directory Replication Scope
1. On the **Active Directory Zone Replication Scope** configuration page, select the option: **To all DNS servers running on domain controllers in this domain: corp.oaktowncs.com**. This setting ensures that every local domain controller running DNS in our specific network partition will stay automatically synced with these pointers.
2. Click **Next**.

<img width="621" height="425" alt="4" src="https://github.com/user-attachments/assets/61240cde-fbfb-4c4b-9dca-f07dfc304755" />

### Step 5: Specify IP Version and Network Identity
1. On the **Reverse Lookup Zone Name** page, select **IPv4 Reverse Lookup Zone**.
2. Click **Next**.

<img width="726" height="434" alt="5" src="https://github.com/user-attachments/assets/dd72f76a-3fc7-461c-8454-66e026d13480" />

3. On the next screen, keep the selection on **Network ID:** and enter the first three octets of your network range: **`192.168.1`**. 
4. Click **Next**.

<img width="619" height="426" alt="6" src="https://github.com/user-attachments/assets/89a20e14-f9b9-40a1-ab46-d807919de17f" />

### Step 6: Define Dynamic Update Policies
1. On the **Dynamic Update** screen, select **Allow only secure dynamic updates (recommended for Active Directory)**. Choosing this prevents rogue network equipment or users from spoofing or injecting unauthorized records into our zone data.
2. Click **Next**.

<img width="649" height="428" alt="7" src="https://github.com/user-attachments/assets/c18a5433-c8b8-4a29-81f6-77cab8c4e45d" />



