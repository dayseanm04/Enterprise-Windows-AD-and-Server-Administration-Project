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

