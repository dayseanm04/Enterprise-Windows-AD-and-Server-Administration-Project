# 01 Create AD Users Account Script

## Description

The purpose of the script is to automate the creation of Active Directory Users accounts instead of using the GUI.

## AI Contribution
Chat GPT generated the whole script based on the prompt I used. Find the prompt [**here**](../02-Prompt-Engineering/01-Generate-PowerShell-Script-for-AD-User-Creation-Using-AI.md)

## Script Generated

```powershell
Import-Module ActiveDirectory

# Base domain and OU path
$baseOU = "OU=users-ou,DC=corp,DC=company,DC=com"

# Departments
$departments = @("HR", "Administration", "IT", "Finance", "Customer Service")

# Default password (change as needed)
$securePassword = ConvertTo-SecureString "P@ssw0rd123!" -AsPlainText -Force

foreach ($dept in $departments) {
    
    # Construct OU path
    $ouPath = "OU=$dept,$baseOU"
    
    for ($i = 1; $i -le 2; $i++) {
        
        # User details
        $firstName = "$dept-User$i"
        $lastName = "Test"
        $name = "$firstName $lastName"
        $samAccountName = ($dept.Substring(0,3) + "user" + $i).ToLower()
        $userPrincipalName = "$samAccountName@corp.company.com"

        # Create user
        New-ADUser `
            -Name $name `
            -GivenName $firstName `
            -Surname $lastName `
            -SamAccountName $samAccountName `
            -UserPrincipalName $userPrincipalName `
            -Path $ouPath `
            -AccountPassword $securePassword `
            -Enabled $true `
            -ChangePasswordAtLogon $true

        Write-Host "Created user: $name in $dept OU"
    }
}
```
