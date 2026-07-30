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
