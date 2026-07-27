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
