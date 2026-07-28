# Share Folders Using PowerShell

## Overview
I already shared the Company-Folder manually using the GUI, but doing that one folder at a time doesn't scale especially with many folders. So instead of clicking through Server Manager for each one, I used PowerShell to share the rest of the folders.

- Opened File Explorer
- Clicked Network
- Click **OTCS-DC01**

<img width="621" height="412" alt="1" src="https://github.com/user-attachments/assets/fb48876b-1ab9-431c-9008-ed2a0eeb4a98" />

<img width="639" height="415" alt="2" src="https://github.com/user-attachments/assets/7d88777a-2051-41ad-b985-4e42cbc5ac8f" />

<img width="808" height="408" alt="3" src="https://github.com/user-attachments/assets/854b7e42-83b7-4056-8de1-3079551dcfcb" />

<img width="717" height="422" alt="4" src="https://github.com/user-attachments/assets/0ce9ca21-a78c-498a-acb0-52375d0628ea" />

- Opened one of the files to view its content

### PowerShell Script

- [Click Here to View the PowerShell script](../../12-Powershell-Scripts/06-PowerShell-Script-To-Share-Folders-Using-PowerShell.md)

## Running the Script
```powershell
./sharefolders.ps1
```

