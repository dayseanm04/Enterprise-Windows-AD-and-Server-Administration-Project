# 02 - VLAN and IP Addressing Design  

## 📌 Overview  

This document defines the VLAN and IP addressing design for **Oak Town Corporate Services**. Since I am building this project virtually using Hyper-V.

I will use the **Hyper-V virtual switches** to simulate network segmentation.

The network is segmented by **department and floor**, using VLANs and **VLSM (/28 subnets)** to efficiently allocate IP addresses while maintaining separation between departments.


## 🏢 Building Layout  

The company operates in **one building with two floors**:
- 1st Floor – HR and Administration  
- 2nd Floor – Finance, Customer Service, and IT  

Each department is assigned:

- A dedicated VLAN  
- A /28 subnet  
- 14 usable host addresses 

Formula used:
- 2^4 = 16 addresses
- 16 - 2 (Network & Broadcast) = 14 usable hosts


# 🥇 1st Floor VLAN Design  

## 👥 HR Department  

- **VLAN ID:** 110  
- **Subnet:** 192.168.1.0/28  
- **Network Address:** 192.168.1.0  
- **Usable Range:** 192.168.1.1 – 192.168.1.14  
- **Broadcast Address:** 192.168.1.15


## 🗂 Administration Department  
- **VLAN ID:** 150  
- **Subnet:** 192.168.1.16/28  
- **Network Address:** 192.168.1.16  
- **Usable Range:** 192.168.1.17 – 192.168.1.30  
- **Broadcast Address:** 192.168.1.31  

# 🥈 2nd Floor VLAN Design  

## 💰 Finance Department  
- **VLAN ID:** 210  
- **Subnet:** 192.168.2.0/28  
- **Network Address:** 192.168.2.0  
- **Usable Range:** 192.168.2.1 – 192.168.2.14  
- **Broadcast Address:** 192.168.2.15  

## 📞 Customer Service Department  
- **VLAN ID:** 220  
- **Subnet:** 192.168.2.16/28  
- **Network Address:** 192.168.2.16  
- **Usable Range:** 192.168.2.17 – 192.168.2.30  
- **Broadcast Address:** 192.168.2.31  

## 🖥 IT Department  
- **VLAN ID:** 250  
- **Subnet:** 192.168.2.32/28  
- **Network Address:** 192.168.2.32  
- **Usable Range:** 192.168.2.33 – 192.168.2.46  
- **Broadcast Address:** 192.168.2.47  


# 🌐 VLSM Design Strategy  

This network uses **Variable Length Subnet Masking (VLSM)** to efficiently allocate address space while avoiding IP waste.

Each department receives a /28 subnet, which provides:
- 14 usable IP addresses  
- Logical separation  

### This VLAN and IP addressing design ensures:

- Network segmentation by Department and Floor





