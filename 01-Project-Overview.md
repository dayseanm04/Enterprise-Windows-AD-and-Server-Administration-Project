# 🏢 Enterprise Windows AD & Server Administration Project  

## 📌 Project Overview  

In this project i will be designing, deploying, and administering a **centralized Windows Server 2019 enterprise infrastructure** using Microsoft **Hyper-V** to support a small-to-medium sized organization with approximately 20–25 Windows client computers.

The project simulates a real-world business where centralized identity management, secure network services, endpoint control, and administrative automation are required to efficiently manage users, devices, and company resources.

The infrastructure is built using industry-standard Microsoft technologies including:
- Hyper-V Virtualization
- Active Directory Domain Services (AD DS)  
- DNS and DHCP  
- Group Policy Management  
- Windows Server Security Features  
- Hyper-V Virtualization  
- Backup and Recovery Solutions  

The primary goal of this project is to demonstrate practical Windows Server administration skills and enterprise infrastructure design best practices.

---

## 🏢 Company Profile  

The project simulates a growing small-to-medium business with five departments:

| Department | Number of Employees |
|------------|--------------------|
| Finance | 5 |
| Human Resources (HR) | 5 |
| Administration | 5 |
| IT Department | 3 |
| Customer Service | 2 |

Each department requires:
- Secure access to shared resources  
- Role-based permissions  
- Centralized authentication  
- Department-specific Group Policy settings  
- Data protection and backup solutions  

---

## Infrastructure Architecture
The environment will be deployed using Hyper-V virtualization.

### Virtual Infrastructure Design
The project will include:

- 1 Hyper-V VM for the Windows Server 2019
- A Domain Controller (AD DS, DNS)
- A DHCP Server
- 10-20 Domain-joined Windows client machines


Virtual networking will be configured using:
- Hyper-V Virtual Switches (External / Internal as needed)
- Proper IP addressing design
- Logical network segmentation


##  Infrastructure Goals 

### 🔐 Centralized Identity Management
- Domain-based authentication  
- Organizational Unit (OU) structure by department  
- Role-based security groups  

### 🌐 Core Network Services
- Internal DNS name resolution  
- DHCP address management  
- Structured IP addressing design 

### 🛡 Security Implementation
- Password policies and account lockout policies  
- Windows Defender configuration  
- Windows Firewall rule enforcement  
- Role-Based Access Control (RBAC)

### 💻 Endpoint Management
- Domain-joined Windows client machines  
- Group Policy enforcement  
- Department-specific configuration policies

### ⚙️ Automation & Administration
- PowerShell scripting for user creation and management  
- Remote management tools  
- Centralized server administration  

### 💾 Business Continuity
- Backup strategy implementation  
- Recovery procedures  
- Disaster recovery planning  

---

## 💼 Business Justification  

As organizations grow, managing users and computers individually becomes inefficient and increases security risks.  

This project demonstrates how Windows Server 2019 can:

- Increase administrative efficiency  
- Improve overall security posture  
- Standardize user environments  
- Reduce configuration errors  
- Provide centralized control over enterprise resources  

---

## 🖥 Technical Scope  

This project focuses on:

- On-premise Windows Server 2019   
- Active Directory Domain environment  
- Virtualized infrastructure using Hyper-V  
- Enterprise administrative best practices  
- Structured documentation and change management  

Cloud integration may be considered for future.
