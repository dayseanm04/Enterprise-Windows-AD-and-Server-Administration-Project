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

