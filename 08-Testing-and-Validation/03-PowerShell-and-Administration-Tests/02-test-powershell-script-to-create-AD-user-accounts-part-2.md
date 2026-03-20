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

I attempted to log in as **finuser3**

<img width="698" height="695" alt="33" src="https://github.com/user-attachments/assets/08c78081-2d54-4d77-98af-45aaf433707f" />

I was prompted to change the passsword, I changed it

<img width="726" height="718" alt="34" src="https://github.com/user-attachments/assets/322230fb-97db-4762-bf55-d22e1a068ce7" />

<img width="749" height="491" alt="35" src="https://github.com/user-attachments/assets/684ee86a-3224-41ef-9b23-64ff557b0d12" />

The login failed.

<img width="598" height="435" alt="36" src="https://github.com/user-attachments/assets/757864d8-167b-402e-904d-58c49b34dbd9" />

---

After executing the updated PowerShell script and verifying user account creation, login attempts failed.

This section documents my troubleshooting process.

## Troubleshoot 1 – Verify if Issue is Script-Related

### Action

- Deleted all user accounts created by the script  
- Manually created a test user account in Active Directory  

Steps:

1. Open **Active Directory Users and Computers**
2. Navigate to User-OU, Administration
3. Right-click **New, User**

<img width="854" height="588" alt="40" src="https://github.com/user-attachments/assets/9544d3b8-6241-4da1-8b47-d051c5d7ce6a" />

click **Next**

<img width="841" height="581" alt="41" src="https://github.com/user-attachments/assets/6c6a8bd4-f0e3-40c3-88b8-da5f23b4f410" />

Click **Finish**
<img width="848" height="505" alt="42" src="https://github.com/user-attachments/assets/742c1828-9b42-421d-bce2-d0e3bb81535f" />

I attempted to log in as **john.doe**

<img width="708" height="530" alt="43" src="https://github.com/user-attachments/assets/ea92291b-4fd8-4fad-b9c6-1e8a0dbc4514" />

The login failed.

<img width="598" height="435" alt="36" src="https://github.com/user-attachments/assets/757864d8-167b-402e-904d-58c49b34dbd9" />

### Conclusion

The issue is **not related to the PowerShell script**  
It affects user accounts in general

## Troubleshoot 2 – Check Account Properties

### Action

1. Open **Active Directory Administrative Center**
2. Navigated to corp → Users-OU → Administration
3. Right-click **john doe**, then  **Properties**

<img width="810" height="511" alt="TS1" src="https://github.com/user-attachments/assets/40bb4207-3a93-43b2-9f17-80e6a9b2cc12" />

<img width="1015" height="477" alt="TS2" src="https://github.com/user-attachments/assets/e55b105c-3ded-4827-aec9-3332aed666ff" />

### Finding

- User SamAccountName was set to **corp**

### Action Taken

Attempted login using: corp\john.doe

<img width="711" height="694" alt="TS3" src="https://github.com/user-attachments/assets/93ee2cdc-e4ed-4468-895a-2047f5ee799a" />

Login Failed

<img width="778" height="660" alt="TS4" src="https://github.com/user-attachments/assets/d4b1df00-1771-4712-8341-6ce787b67b2f" />

## Troubleshoot 3 – Change User SamAccountName from corp ot OTCSCORP

### Action

1. In **Active Directory Administrative Center**
2. Edit user properties
3. Change corp to OTCSCORP

<img width="1009" height="447" alt="TS5" src="https://github.com/user-attachments/assets/47b8fd15-23c8-434f-a2dc-a0a700303c18" />

### Retest Login with OTCSCORP\john.doe

<img width="862" height="705" alt="TS6" src="https://github.com/user-attachments/assets/231ae26b-796f-4bbb-bbc3-c8debe8d5c5f" />

<img width="846" height="662" alt="TS7" src="https://github.com/user-attachments/assets/191ff84e-c11b-498a-b3e6-d7a41385a6e2" />

---

### Result

- Login still failed  

## Troubleshoot 4 – Investigate Network Configuration

### Observation

- Test server is using OTCS-TEST-SW (Internal Virtual Switch)

### Step 1 – Check IP Configuration

Run:

```powershell
ipconfig /all
```

<img width="868" height="495" alt="TS8" src="https://github.com/user-attachments/assets/1724c982-b707-454e-b415-83cb160fc665" />

### Finding

The Test Server is using APIPA address

### Step 2 – Configure Host Machine IP


1. Open Settings then click on **Network & Internet**
2. Click on **Edit IP Assignment**

<img width="593" height="344" alt="TS12" src="https://github.com/user-attachments/assets/d47467c1-55d4-43cf-810e-12c6f9387c5a" />

- Select: Manual, enable IPv4
- I changed my hostmachine IP to 169.254.130.49/16

<img width="502" height="370" alt="TS13" src="https://github.com/user-attachments/assets/a9a8e042-79a2-488c-9b76-f591982f387e" />

Attempted to login

<img width="862" height="705" alt="TS6" src="https://github.com/user-attachments/assets/231ae26b-796f-4bbb-bbc3-c8debe8d5c5f" />

<img width="846" height="662" alt="TS7" src="https://github.com/user-attachments/assets/191ff84e-c11b-498a-b3e6-d7a41385a6e2" />

Login still failed 
