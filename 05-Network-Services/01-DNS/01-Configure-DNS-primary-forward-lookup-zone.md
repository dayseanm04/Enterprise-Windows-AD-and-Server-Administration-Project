# Configure DNS Primary Forward Lookup Zone

## Overview
A Forward Lookup Zone is a fundamental component of the Domain Name System (DNS) that resolves human-readable hostnames (such as **`server.corp.oaktowncs.com`**) into IP addresses. 

---

## Objectives
- Configure a primary forward zone

---

## Environment
- **Domain:** corp.oaktowncs.com
- **Tools Used:**
  - Server Manager
  - DNS Manager Console
 
---

## Step-by-Step Configuration

### Step 1: Open DNS Manager
1. Open **Server Manager**.
2. Click **Tools** in the top navigation bar.
3. Select **DNS** from the drop-down menu.

<img width="391" height="208" alt="1" src="https://github.com/user-attachments/assets/781e6a6b-f35f-4830-86ea-6149fa0ea643" />

### Step 2: Initialize New Zone Wizard
1. In the **DNS Manager** console tree, expand your server node (`OTCS-DC01.corp.oaktowncs`).
2. Right-click on **Forward Lookup Zones** and select **New Zone...**

<img width="650" height="283" alt="2" src="https://github.com/user-attachments/assets/c7b6a027-3c2a-47c9-9778-34a7cec2d300" />

### Step 3: Configure Zone Type
1. On the **New Zone Wizard** welcome page, click **Next**.
2. Select **Primary zone** as the type of zone to create.
3. Check the box to **Store the zone in Active Directory (available only if DNS server is a writeable domain controller)**.
4. 
<img width="502" height="402" alt="3" src="https://github.com/user-attachments/assets/05b43976-9c19-4fa3-9d2b-681f26764d40" />

### Step 4: Define Replication Scope
1. On the **Active Directory Zone Replication Scope** page, select the radio button for **To all DNS servers running on domain controllers in this domain: corp.oaktowncs.com**.
2. Click **Next**.

<img width="498" height="388" alt="4" src="https://github.com/user-attachments/assets/4306e4a2-eb07-4b38-bc73-2421a21ca010" />

### Step 5: Specify Zone Namespace
1. On the **Zone Name** page, type `corp.oaktowncs.com` into the **Zone name:** field.
2. Click **Next**.




