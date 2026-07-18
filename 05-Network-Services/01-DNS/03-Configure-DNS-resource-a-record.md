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

<img width="762" height="374" alt="2" src="https://github.com/user-attachments/assets/2e6132d0-c8e2-4005-bf04-b15bbad300f6" />

### Step 3: Create the new host
1. In the **New Host** dialog window, enter the following parameters
2. Check the box labeled **Create associated pointer (PTR) record**.
3. Check the box labeled **Allow any unauthenticated user to update DNS records with the same owner name**.

<img width="667" height="453" alt="3" src="https://github.com/user-attachments/assets/aba2fbf9-3d8e-4be2-b15e-a8947ac54448" />

4. Click **Add Host**
5. When the success dialog popups stating *"The host record comp-a-test.corp.oaktowncs.com was successfully created."*, click **OK**.
6. Click **Done**.




