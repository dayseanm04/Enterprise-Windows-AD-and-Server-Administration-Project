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


