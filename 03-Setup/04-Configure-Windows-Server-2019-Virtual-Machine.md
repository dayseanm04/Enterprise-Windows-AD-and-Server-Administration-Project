# 04 – Configure Windows Server 2019 Virtual Machine  

##  Overview  

In this step, I will configure a new Virtual Machine for the **Windows Server 2019** using **Hyper-V Manager**.

This VM will serve as the foundation for:
- Active Directory Domain Services (AD DS)

---

##  Objective  

Create and configure a Windows Server 2019 VM with:
- Generation 2
- 6 GB RAM (Dynamic Memory enabled)
- 100 GB virtual hard disk
- Windows Server 2019 ISO attached
- Default Virtual Switch (temporary)

## Tools Used  

- Hyper-V Manager  
- Windows Server 2019 ISO
- Dedicated VHD storage folder (`C:\Win-2019-SRV-VHD`)

---

##  Step-by-Step 

###  Step 1 - Open Hyper-V Manager  

1. Click **Start**
2. Search for **Hyper-V Manager**
3. Open the application

<img width="774" height="296" alt="1" src="https://github.com/user-attachments/assets/c7c3717c-072a-4fb5-a4bc-d860d81d4144" />

###  Step 2 - Create New Virtual Machine  
1. Right-click on your computer name  
2. Click **New**
3. Select **Virtual Machine**

<img width="569" height="270" alt="2" src="https://github.com/user-attachments/assets/03b25b57-22e3-4ba4-b252-606ebe5fc6ab" />



