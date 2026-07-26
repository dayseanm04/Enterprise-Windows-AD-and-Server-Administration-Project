# Configure File Permissions Using PowerShell

## Overview

Configure NTFS file permissions so each security group only has the access to the files they need. Rather than setting permissions manually through the GUI, I wrote a PowerShell script using `icacls` to grant permissions based on data imported from a CSV file.

## Requirements
A CSV file containing the users and security groups. It's stored in the repo here:
- `14-CSV-files/OTCS-Users.csv`

## PowerShell Script

Saved as `fileperm.ps1`:
