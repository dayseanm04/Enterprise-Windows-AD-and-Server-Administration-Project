# 02 – VLAN and IP Addressing Design  

## 📌 Overview  

This document defines the VLAN and IP addressing design for **Oak Town Corporate Services**. Since I am building this project virtually using Hyper-V.

I will use the **Hyper-V virtual switches** to simulate network segmentation.

The network is segmented by **department and floor**, using VLANs and **VLSM (/28 subnets)** to efficiently allocate IP addresses while maintaining separation between departments.

---

## 🏢 Building Layout  

The company operates in **one building with two floors**:
- 1st Floor – HR and Administration  
- 2nd Floor – Finance, Customer Service, and IT  

Each department is assigned:
