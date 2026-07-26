# Configure File Permissions Using PowerShell

## Overview

Configure NTFS file permissions so each security group only has the access to the files they need. Rather than setting permissions manually through the GUI, I wrote a PowerShell script using `icacls` to grant permissions based on data imported from a CSV file.

## Requirements
A CSV file containing the security groups. It's stored in the repo here:
- [14-CSV-files/OTCS-Security-Groups.csv](../../14-CSV-files/OTCS-Security-Groups.csv)

## PowerShell Script
- [Click Here to View the powershell script](../../12-Powershell-Scripts/04-PowerShell-Script-To-Configure-File-Permissions.md)


Saved as `fileperm.ps1`:

## PowerShell Script



### How it works
- `$SecGroups` imports the list of security groups from a CSV file.
- Each folder (`Company`, `Customer-Services`, `Finance`, `HR`, `IT`) has its own function that loops through the imported security groups and uses a `switch` statement to match the relevant group name.
- `icacls` is used to grant permissions on each file — `(R)` for Read-only access, `(F)` for Full Control — depending on the security group and folder.
- `break` stops the switch from checking further conditions once a match is found.
- At the bottom, each function is called

### Notes
- File and folder paths are specific to this project — update them to match your own environment if reusing this script.
- Permissions can also be configured through the Windows GUI; I chose PowerShell here specifically to practice scripting.

## Running the Script
I saved the script in my ps-scripts folder

```powershell
./configure-file-permissions.ps1
```

The script ran successfully:

<img width="911" height="740" alt="1" src="https://github.com/user-attachments/assets/d20d569d-590a-4bc0-8a4b-7bae3bf72304" />

## Verify
I checked the file permissions on the files in the Company folder using `icacls`:

<img width="891" height="656" alt="2" src="https://github.com/user-attachments/assets/39ccf8f2-60b8-4e56-8cbc-96d22f903ec0" />



