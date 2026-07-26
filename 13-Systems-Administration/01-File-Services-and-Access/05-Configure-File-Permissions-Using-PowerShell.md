# Configure File Permissions Using PowerShell

## Overview

Configure NTFS file permissions so each security group only has the access to the files they need. Rather than setting permissions manually through the GUI, I wrote a PowerShell script using `icacls` to grant permissions based on data imported from a CSV file.

## Requirements
A CSV file containing the users and security groups. It's stored in the repo here:
- `14-CSV-files/OTCS-Users.csv`

## PowerShell Script

Saved as `fileperm.ps1`:

## PowerShell Script

Saved as `configure-file-permissions.ps1`:

```powershell
$SecGroups = Import-Csv "$HOME\Desktop\csv-files\secgroups.csv"

$success = @{
    ForegroundColor = "Green"
    BackgroundColor = "Black"
}

# Configure permissions for files in Company folder
function CompanyFolder {
    foreach ($sg in $SecGroups.SecGroup) {   # Loops through every security group
        switch ($sg) {
            { $_ -eq "EveryUser-Sec-G" } {   # $_ represents the value of $sg
                Write-Host ""
                Write-Host "Granting $_ Read Permission for the files in the Company-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Company-Folder\policies.txt" /grant "$($_):(R)"
                icacls "$HOME\Desktop\shared-folders\Company-Folder\holiday-schedule.txt" /grant "$($_):(R)"
                break
            }
            { $_ -eq "HR-Sec-G" } {
                Write-Host ""
                Write-Host "Granting $_ Full Access to the files in the Company-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Company-Folder\policies.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\Company-Folder\holiday-schedule.txt" /grant "$($_):(F)"
            }
        }
    }
}

# Configure permissions for files in Customer-Service folder
function CustomerServicesFolder {
    foreach ($sg in $SecGroups.SecGroup) {
        switch ($sg) {
            { $_ -eq "Customer-Service-Sec-G" } {
                Write-Host " "
                Write-Host "Granting $_ Full Access to the files in the Customer-Service-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Customer-Services-Folder\faq.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\Customer-Services-Folder\support-temp.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Configure permissions for files in Finance folder
function FinanceFolder {
    foreach ($sg in $SecGroups.SecGroup) {
        switch ($sg) {
            { $_ -eq "Finance-Sec-G" } {
                Write-Host " "
                Write-Host "Granting $_ Full Access to the files in the Finance-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Finance-Folder\payroll.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\Finance-Folder\tax-doc.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Configure permissions for files in HR folder
function HRFolder {
    foreach ($sg in $SecGroups.SecGroup) {
        switch ($sg) {
            { $_ -eq "HR-Sec-G" } {
                Write-Host " "
                Write-Host "Granting $_ Full Access to the files in the HR-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\HR-Folder\hiring-doc.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\HR-Folder\onboarding-doc.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Configure permissions for files in IT folder
function ITFolder {
    foreach ($sg in $SecGroups.SecGroup) {
        switch ($sg) {
            { $_ -eq "IT-Sec-G" } {
                Write-Host " "
                Write-Host "Granting $_ Full Access of the files in IT-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\IT-Folder\documentation.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\IT-Folder\setup-guides.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Call the functions
CompanyFolder
CustomerServicesFolder
FinanceFolder
HRFolder
ITFolder
```


