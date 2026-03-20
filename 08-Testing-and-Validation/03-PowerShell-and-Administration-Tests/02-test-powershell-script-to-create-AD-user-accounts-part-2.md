# 02 – Test PowerShell Script to Create AD User Accounts Part 2

## Overview

I will test the PowerShell script generated using AI to automate the creation of Active Directory user accounts. But this time i will modify the script

The goal of this test was to:

- Validate that the script successfully creates user accounts  
- Review the accounts it created  
- Confirm the created users accounts can login

The scrip I ran:

```powershell
Import-Module ActiveDirectory

# Base domain and OU path
$baseOU = "OU=users-ou,DC=corp,DC=oaktowncs,DC=com"

# Departments
$departments = @("HR", "Administration", "Finance", "Customer Service")

# Default password (change as needed)
$securePassword = ConvertTo-SecureString "P@ssw0rd123!" -AsPlainText -Force

foreach ($dept in $departments) {
    
    # Construct OU path
    $ouPath = "OU=$dept,$baseOU"
    
    for ($i = 2; $i -le 4; $i++) {
        
        # User details
        $firstName = "$dept-User$i"
        $lastName = "Test"
        $name = "$firstName $lastName"
        $samAccountName = ($dept.Substring(0,3) + "user" + $i).ToLower()
        $userPrincipalName = "$samAccountName@corp.oaktowncs.com"

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
	-PasswordNeverExpires $false `
            -ChangePasswordAtLogon $false

        Write-Host "Created user: $name in $dept OU"
    }
}

```
