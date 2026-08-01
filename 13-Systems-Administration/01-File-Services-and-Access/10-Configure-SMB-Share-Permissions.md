# Configure SMB Share Permissions

## Overview
This is the continuation from [**01-Troubleshoot-Read-Only-and-Share-Permissions.md**](../../09-Troubleshooting/02-Files-and-Folders-Troubleshooting/01-Troubleshoot-Read-Only-and-Share-Permissions.md) — I found there that an HR user couldn't write files to the HR-Folder because I'd only configured NTFS permissions, not the SMB share permissions. I fixed HR-Folder through the GUI there. Here I'm doing the same thing for the rest of the folders, first showing the GUI method, then a PowerShell script to do it for all of them at once.

## Using the GUI (HR-Folder)
1. Open File Explorer, click **Network**, click **OTCS-DC01**.
2. Right-click the **HR-Folder**, click **Properties**.
3. Click the **Sharing** tab.

<img width="554" height="426" alt="1" src="https://github.com/user-attachments/assets/b4c231e0-32c4-4f6e-9f13-96327dc0e39b" />

Clicked the **Advanced Sharing...** tab:

<img width="565" height="440" alt="2" src="https://github.com/user-attachments/assets/ffdec628-b726-486c-9359-2def64c50efd" />

Clicked **Permissions**, clicked **Add**, added `HR-Sec-G`, and gave it **Full Control**.

<img width="540" height="499" alt="3" src="https://github.com/user-attachments/assets/69b4c37c-e379-4a79-953d-a09f8ee282e3" />

Clicked **OK**, **OK**.

## Using PowerShell (Remaining Folders)
Doing this one folder at a time through the GUI isn't practical for the rest of the shares, so I wrote a PowerShell to automate it for `IT-Folder`, `Finance-Folder`, and `Customer-Services-Folder`.

## 2 Using the GUI (Company-Folder)

### PowerShell Script

- [Click Here to View the PowerShell script](../../12-Powershell-Scripts/07-PowerShell-Script-Configure-SMB-Share-Permissions.md)

### How it works
- `$SecGroups` imports the security groups from the CSV file.
- `$success` is the same green-on-black `Write-Host` hashtable I've used in the other scripts.
- `$folders` lists the shares I'm checking with `Get-SmbShareAccess` before granting anything, just to see the starting state.
- `GrantAccess` loops through the security groups and matches each one to its folder with a `switch`, then uses `Grant-SmbShareAccess` to give that group Full Control at the share level.
- Note: `HR-Sec-G` isn't in this switch — I already fixed HR-Folder's share permissions through the GUI above, so the script only needed to cover the remaining three folders.

Ran the script:

<img width="827" height="467" alt="Screenshot 2026-07-29 200611" src="https://github.com/user-attachments/assets/b70cbc3b-1643-44ba-861f-eb95316a7971" />

## Removing Default "Everyone" Access
By default, `Everyone` had Read access to these shares. Since each folder now has its correct security group with Full Control, I don't need `Everyone` on there too — so I added a line to revoke it:

```powershell
Revoke-SmbShareAccess -Name $folders[number] -AccountName "Everyone" -Force
```


