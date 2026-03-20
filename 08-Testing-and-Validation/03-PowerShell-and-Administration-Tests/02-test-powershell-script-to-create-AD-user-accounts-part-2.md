# 02 – Test PowerShell Script for creating AD User Accounts Part 2

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

<img width="812" height="703" alt="30" src="https://github.com/user-attachments/assets/31881a18-2779-4d31-a67d-b6d805a900c7" />

### Verify user accounts were created

<img width="816" height="509" alt="31" src="https://github.com/user-attachments/assets/1f44bbbb-a6b4-433f-936b-7a6f1c48b6cf" />

### Review finuser3 account

<img width="766" height="554" alt="32" src="https://github.com/user-attachments/assets/a064a8b2-4ad1-45db-aa0a-97545aaf228b" />

I attempted to sign in as **finuser3**

<img width="698" height="695" alt="33" src="https://github.com/user-attachments/assets/08c78081-2d54-4d77-98af-45aaf433707f" />

I was prompted to change the passsword, I changed it

<img width="726" height="718" alt="34" src="https://github.com/user-attachments/assets/322230fb-97db-4762-bf55-d22e1a068ce7" />

<img width="749" height="491" alt="35" src="https://github.com/user-attachments/assets/684ee86a-3224-41ef-9b23-64ff557b0d12" />


















