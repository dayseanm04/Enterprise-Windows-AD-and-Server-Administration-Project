# Verifying DNS Reverse Lookup Functionality

## Overview
I will test and verify the forward and reverse lookup functionalities of the Windows Server DNS deployment. Testing ensures that the IP-to-hostname (reverse) resolutions are running properly across the network.

> **Pre-configuration Note:** During the static IP configuration of the Domain Controller (`OTCS-DC01`), I configured the primary DNS server to the loopback address (`127.0.0.1`).

---

## Environment
- **Domain Controller:** `OTCS-DC01` (IP: `192.168.1.2`, Domain: `corp.oaktowncs.com`)
- **Test Client Machine:** `comp-a-test` (IP: `192.168.1.3`)

---

## Verification Procedures

### Step 1: Execute Reverse Lookup Tests via Ping from the Domain Controller
1. On the **OTCS-DC01** domain controller, run **Windows PowerShell**.

<img width="778" height="517" alt="1" src="https://github.com/user-attachments/assets/d54b40f6-41fd-4766-ab75-9c84f876e7d9" />

### Step 2: Validate Name Resolution using nslookup on the Domain Controller

<img width="625" height="371" alt="2" src="https://github.com/user-attachments/assets/dc5452f8-0999-4c3e-bd03-ab4ddc05a8db" />

### Step 3: Run Reverse Lookup Tests from the Client Machine (comp-a-test)

<img width="918" height="595" alt="3" src="https://github.com/user-attachments/assets/e117a1bf-2091-4b5e-aed8-4a7fecb619d1" />

### Step 4: Validate DNS Server Resolution using nslookup on the Client Machine

<img width="779" height="358" alt="4" src="https://github.com/user-attachments/assets/eb40b296-e357-4592-b75a-4664a7eb3b4f" />
