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
