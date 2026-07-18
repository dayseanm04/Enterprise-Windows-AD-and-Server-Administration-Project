# Configure a DNS A Record and Associated PTR Record

## Overview
In this task I will configure a Host (A) record. An A record maps a human-readable hostname to an IPv4 address, which is essential for name resolution across the enterprise network. 

In this task, I configured a record for my local host machine which I will be using for testing.

## Objectives
- Navigate Windows Server DNS Manager.
- Create a new Host (A) record inside a targeted domain zone.
- Enable automatically creating a matching reverse-lookup PTR record.

---

## Environment
- **Domain Controller:** OTCS-DC01 (`OTCS-DC01.corp.oaktowncs`)
- **Target Domain Zone:** `corp.oaktowncs.com`
- **Test Machine Hostname:** `comp-a-test`
- **Test Machine IP Address:** `192.168.1.3` (Local Windows host machine)

---

## Step-by-Step Configuration

### Step 1: Open DNS Manager
1. Open **Server Manager**.
2. Click **Tools** in the top navigation bar.
3. Select **DNS** from the drop-down menu.

<img width="391" height="208" alt="1" src="https://github.com/user-attachments/assets/781e6a6b-f35f-4830-86ea-6149fa0ea643" />

### Step 2: Create an A reccord
1. In the **DNS Manager** console tree, expand your server node (`OTCS-DC01.corp.oaktowncs`).
2. Expand the **Forward Lookup Zones** folder.
3. Right-click on your target domain: **corp.oaktowncs.com**.
4. Select **New Host (A or AAAA)...** from the context menu.

