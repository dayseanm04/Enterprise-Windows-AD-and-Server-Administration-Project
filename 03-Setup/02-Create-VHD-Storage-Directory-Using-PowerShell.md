# 02 – Create VHD Storage Directory Using PowerShell  

##  Overview  

In this step, I will crate a dedicated storage directory on my host machine to store the Virtual Hard Disk (VHD) files for Windows Server 2019.

For this project, the VHD storage folder will be created on the **C:\ drive**.

---

##  Objective  

Create a folder named: Win-2019-SRV-VHD
Note: you can use any name but I chose this because it representes the servers VHD

This folder will store the virtual disk files used by Hyper-V.

---

##  Tools Used  

- Windows PowerShell  

## Step-by-Step   

###  Step 1 - Open PowerShell  
1. Click **Start**
2. Search for **PowerShell**
3. Right-click **Windows PowerShell**
3. Right-click **Windows PowerShell**

<img width="745" height="387" alt="10" src="https://github.com/user-attachments/assets/15ed600f-2f41-484e-ac51-f3231ac11545" />

Note: I didnt run Powershell as admin because my accound is already an Admin Account

###  Step 2 - Navigate to the C:\ Drive  

```powershell
cd C:\
```

To confirm current directory (optional): 

```powershell
dir
```

###  Step 3 - Create the VHD Folder

```powershell
mkdir Win-2019-SRV-VHD
```

