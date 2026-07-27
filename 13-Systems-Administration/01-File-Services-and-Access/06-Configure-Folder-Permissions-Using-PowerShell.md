# Configure Folder Permissions Using PowerShell

## Overview
After configuring permissions on individual files, the next step was to configure permissions at the folder level so each security group has the right access to entire shared folders. This also involved moving the `shared-folders` and `csv-files` directories from the Desktop to the `C:\` drive to simplify the file paths used in the script.

## Requirements
A CSV file containing the security groups. It's stored in the repo here:

- [14-CSV-files/OTCS-Security-Groups.csv](../../14-CSV-files/OTCS-Security-Groups.csv)

## Setup

### 1. Move the Folders

```powershell
cd C:\
Move-Item -Path "C:\Users\Administrator\Desktop\shared-folders" -Destination "."
Move-Item -Path "C:\Users\Administrator\Desktop\csv-files" -Destination "."
```

<img width="665" height="389" alt="1" src="https://github.com/user-attachments/assets/51678c5c-6858-46f1-b019-083c33e820e1" />

### PowerShell Script

- [Click Here to View the PowerShell script](../../12-Powershell-Scripts/05-PowerShell-Script-To-Configure-Folder-Permissions.md)

### How it works
- `$SecGroups` imports the list of security groups from the CSV file at `C:\csv-files\secgroups.csv`.
- The `ShrdFolderPerm` function loops through each imported security group and uses a `switch` statement to match the group name.
- `icacls` grants permissions at the **folder** level this time (rather than per file) — `EveryUser-Sec-G` gets Read & Execute (`RX`) on the Company folder, while each department's security group gets Full Control (`F`) on its own folder. `HR-Sec-G` gets Full Control on the Company folder.

