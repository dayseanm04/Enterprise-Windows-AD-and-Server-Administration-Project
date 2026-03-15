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

Note: I didnt run Powershell as admin because my account is already an Admin Account

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

<img width="829" height="356" alt="11" src="https://github.com/user-attachments/assets/9ea2c5c1-9b8e-41f8-aa35-94598ce29d68" />

### Step 4 – Verify the Folder was created

```powershell
dir
```

<img width="767" height="429" alt="12 (2)" src="https://github.com/user-attachments/assets/fa4821f9-0154-4a46-8b96-6da3643721ca" />

Open File Explorer then Navigate to This PC then the **`C:\`** Folder

<img width="790" height="363" alt="12" src="https://github.com/user-attachments/assets/239b1e28-9e21-4e55-b763-0fe9ef6f4d0c" />

### ✅ Next Click [here for 03-Create-ISO-Directory-Using-PowerShell.md](/03-Setup/03-Create-ISO-Directory-Using-PowerShell.md)
