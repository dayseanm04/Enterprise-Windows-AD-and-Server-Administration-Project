# Manually Creating a DNS Pointer (PTR) Record

## Overview

In this task I will configure a Pointer (PTR) record. 

While PTR records are often auto-generated alongside Host (A) records, you can create it manualy.

## Objectives
- Navigate Windows Server DNS Manager.
- Create a new PTR record inside a targeted domain zone.

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

### Step 2: Access the Target Reverse Lookup Zone
1. In the **DNS Manager** console tree, expand `OTCS-DC01.corp.oaktowncs`.
2. Click to expand the **Reverse Lookup Zones** directory.
3. Select **1.168.192.in-addr.arpa**.
4. Right-click on any empty space within the right-hand details pane of the zone workspace.
5. Click on **New Pointer (PTR)...** from the contextual menu.

<img width="762" height="326" alt="2" src="https://github.com/user-attachments/assets/357e91f7-c091-49eb-9891-1a28f7024a96" />

### Step 3: Configure the Resource Record Parameters
1. In the **New Resource Record** dialog window under the Pointer (PTR) tab, fill in the following properties
2. Check the configuration box at the bottom labeled: **Allow any unauthenticated user to update all DNS records with the same name. This setting applies only to DNS records for a new name.**
3. Click **OK**.

<img width="662" height="490" alt="3" src="https://github.com/user-attachments/assets/0fb5f287-f5d1-4d2e-bd2a-d2a4db36c582" />

<img width="759" height="272" alt="23" src="https://github.com/user-attachments/assets/feaef992-33d3-490e-a8c9-616938d370ac" />



