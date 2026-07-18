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
