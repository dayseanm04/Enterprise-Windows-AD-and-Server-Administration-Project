# 02 - VLAN and IP Addressing Design  

## 📌 Overview  

This document defines the VLAN and IP addressing design for **Oak Town Corporate Services**. Since I am building this project virtually using Hyper-V.

I will use the **Hyper-V virtual switches** to simulate network segmentation.

The network is segmented by **department and floor**, using VLANs and **VLSM (/27 subnets)** to efficiently allocate IP addresses while maintaining separation between departments.

---

## 🏢 Building Layout  

The company operates in **one building with two floors**:
- 1st Floor – HR and Administration  
- 2nd Floor – Finance, Customer Service, and IT  

Each department is assigned:

- A dedicated VLAN  
- A /27 subnet  
- 30 usable host addresses 

Formula used:
- 2^5 = 32 addresses
- 32 - 2 (Network & Broadcast) = 20 usable hosts

---

# 🥇 1st Floor VLAN Design  

## 👥 HR Department  

- **VLAN ID:** 110  
- **Subnet:** 192.168.1.0/27  
- **Network Address:** 192.168.1.0  
- **Usable Range:** 192.168.1.1 – 192.168.1.30  
- **Broadcast Address:** 192.168.1.31  


## 🗂 Administration Department  
- **VLAN ID:** 150  
- **Subnet:** 192.168.1.32/27  
- **Network Address:** 192.168.1.32  
- **Usable Range:** 192.168.1.33 – 192.168.1.62  
- **Broadcast Address:** 192.168.1.63  

---

# 🥈 2nd Floor VLAN Design  

## 💰 Finance Department  
- **VLAN ID:** 210  
- **Subnet:** 192.168.2.0/27  
- **Network Address:** 192.168.2.0  
- **Usable Range:** 192.168.2.1 – 192.168.2.30  
- **Broadcast Address:** 192.168.2.31   


## 📞 Customer Service Department  
- **VLAN ID:** 220  
- **Subnet:** 192.168.2.32/27  
- **Network Address:** 192.168.2.32  
- **Usable Range:** 192.168.2.33 – 192.168.2.62  
- **Broadcast Address:** 192.168.2.63  

## 🖥 IT Department  
- **VLAN ID:** 250  
- **Subnet:** 192.168.2.64/27  
- **Network Address:** 192.168.2.64  
- **Usable Range:** 192.168.2.65 – 192.168.2.94  
- **Broadcast Address:** 192.168.2.95  

---

# 🌐 VLSM Design Strategy  

This network uses **Variable Length Subnet Masking (VLSM)** to efficiently allocate address space while avoiding IP waste.

Each department receives a /27 subnet, which provides:
- 30 usable IP addresses  
- Logical separation  

### This VLAN and IP addressing design ensures:

- Network segmentation by Department and Floor
- Improved security between departments  
- Scalability for future expansion  
