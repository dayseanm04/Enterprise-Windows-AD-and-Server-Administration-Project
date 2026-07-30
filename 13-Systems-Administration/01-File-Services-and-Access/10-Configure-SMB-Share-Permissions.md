# Configure SMB Share Permissions

## Overview
This is the continuation from [01-Troubleshoot-Read-Only-and-Share-Permissions.md](../../09-Troubleshooting/Files-and-Folders-Troubleshooting/01-Troubleshoot-Read-Only-and-Share-Permissions.md) — I found there that an HR user couldn't write files to the HR-Folder because I'd only configured NTFS permissions, not the SMB share permissions. I fixed HR-Folder through the GUI there. Here I'm doing the same thing for the rest of the folders, first showing the GUI method, then a PowerShell script to do it for all of them at once.
