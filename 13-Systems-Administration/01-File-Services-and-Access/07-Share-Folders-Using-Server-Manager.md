# Share Folders Using Server Manager

## Overview
Once I had the folder structure, sample files, and NTFS permissions in place, the next step was actually sharing those folders over the network so people could get access to it. For this project, my VM `Windows-2019-SRV` a domain controller, server, and file server. Below is how I enabled SMB sharing and created a new share using Server Manager's GUI, step by step, the same way I did it.

## Enable SMB Sharing on the Server
1. Open **Control Panel**.
2. Go to **Network and Internet**.
3. Go to **Network and Sharing Center**.
4. Click **Change advanced sharing settings**.
5. Turn on **Network discovery** and **File and printer sharing**.

<img width="777" height="582" alt="1" src="https://github.com/user-attachments/assets/e6ba1fff-d735-4036-be2e-368d82cbd9cc" />

6. Click **Save changes**.

## Create a New Share via Server Manager

### 1. Open File and Storage Services

Open **Server Manager** and click **File and Storage Services**.

<img width="741" height="351" alt="1" src="https://github.com/user-attachments/assets/25c2a5cf-0c60-4a75-8bd6-4fb2519571a1" />

### 2. Go to Shares
Click **Shares**.

<img width="926" height="384" alt="2" src="https://github.com/user-attachments/assets/f0228135-4eba-4ad4-bdfd-709749cc483f" />

### 3. Create a New Share
Click **Tasks** → **New Share...**

<img width="696" height="389" alt="3" src="https://github.com/user-attachments/assets/5f1f478b-783f-4c23-8b07-1d6dd3aad74b" />

### 4. Choose the Share Profile
Select **SMB Share - Quick** and click **Next**.

<img width="764" height="332" alt="4" src="https://github.com/user-attachments/assets/43d0ff16-2298-4519-8650-9ed51668adbf" />

### 5. Select the Folder
Clicked **Custom** and selected the shared folder on the Desktop.
Click **Next**.

<img width="751" height="498" alt="5" src="https://github.com/user-attachments/assets/9152d084-772f-4169-b543-f59333adc48b" />

### 6. Configure Share Name, Description . Local and Remote Path

<img width="766" height="405" alt="6" src="https://github.com/user-attachments/assets/566d8c79-7e10-4c55-b5c2-c47fa6680bc9" />

### 7. Configure Share Settings
Select **Enable access-based enumeration** and **Allow caching of share**, then click **Next**.

<img width="761" height="425" alt="7" src="https://github.com/user-attachments/assets/18f5ad1d-0c99-4497-9f98-879e9d90ae47" />

### 8. Set Permissions
Click **Next**.

<img width="768" height="388" alt="8" src="https://github.com/user-attachments/assets/e53f6449-fe74-4f8e-b09a-840023ab2438" />

### 9. Create the Share
Review the settings, click **Create**, then click **Close**.



