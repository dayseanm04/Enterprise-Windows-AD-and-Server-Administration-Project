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

### Step 3 - Specify Name and Location  
- **VM Name:** `Window-2019-SRV`
- Click **Next**

<img width="703" height="336" alt="3" src="https://github.com/user-attachments/assets/2d97205b-7829-469b-a671-676de71eede2" />

### Step 4 - Select Generation  
- Choose **Generation 2**
- Click **Next**

<img width="701" height="314" alt="4" src="https://github.com/user-attachments/assets/49687ade-e664-4c11-8d14-0a0557e9b164" />

###  Step 5 - Assign Memory  
- Startup Memory: **6096 MB (6 GB)**
- Enable: **Use Dynamic Memory for this virtual machine**
- Click **Next**

<img width="702" height="310" alt="5" src="https://github.com/user-attachments/assets/3a68723c-8754-46d4-8700-07ed868ab2cb" />

> My host machine has 16 GB RAM.

###  Step 6 - Configure Networking  
- Select **Default Switch**
- Click **Next**

> Note: I will configure a dedicated virtual switch later in the project.

<img width="709" height="301" alt="6" src="https://github.com/user-attachments/assets/1fe51889-486a-459d-ac7d-89f048dd7fe1" />

###  Step 7 - Configure Virtual Hard Disk  
- Select **Create a virtual hard disk**
- Location: `C:\Win-2019-SRV-VHD`
- Size: **100 GB**
- Click **Next**

<img width="703" height="296" alt="27" src="https://github.com/user-attachments/assets/379eb996-1498-42d0-9764-d974457d216a" />

> My host machine has ITB SSD. 80GB is OK.





