# 01 - DNS Forward Lookup Validation

## Overview
In this task I will demonstrate how to test and validate the functionality of the DNS Forward Lookup Zone using ping commands on both the domain controller and a remote Windows 11 host.

---

## Objectives
- Perform local forward lookup testing on the domain controller.
- Validate local IPv4 forward lookup resolution on the domain controller.
- Validate remote client-side name resolution and network connectivity from a Windows 11 host.

---

## Environment
- **Domain Controller:** OTCS-DC01 (IP: **`192.168.1.2`**, Loopback: **`127.0.0.1`** / **`::1`**)
- **Client Machine:** Windows 11 Host (IP: **`192.168.1.3`**)
