# 05 - Reset Active Directory User Password Using ADUC, ADAC, and PowerShell

## Overview
This task I will demonstrate how to reset a user's password in Active Directory using multiple methods: Active Directory Users and Computers (ADUC), Active Directory Administrative Center (ADAC), and Windows PowerShell. 

---

## Objectives
- Reset a user password using ADUC
- Reset a user password using ADAC
- Reset a user password using PowerShell
- Disable and re-enable a user account
- Enforce password change at next logon

---

## Environment
- **Domain:** corp.oaktowncs.com
- **Tools Used:**
  - Active Directory Users and Computers (ADUC)
  - Active Directory Administrative Center (ADAC)
  - Active Directory Module for Windows PowerShell

---

### [Click Here for the AD User Accounts Reference](Reference-Oaktown-CS-User-Accounts.md)


### Scenario
**Anna Jones** (Administration Department) forgot her password. The goal is to reset her password using multiple methods.

---

## Method 1: Reset Password Using ADUC

### Steps
1. Open **Server Manager**
2. Click **Tools**
3. Select **Active Directory Users and Computers**
4. Clicked on the domain

<img width="747" height="344" alt="1" src="https://github.com/user-attachments/assets/d9195500-7d5d-4524-9038-ecbe7584c358" />

5. Clicked on **`Users-OU` and `Administration OU`**

<img width="899" height="361" alt="2" src="https://github.com/user-attachments/assets/2db21245-6b95-4837-adc1-0a1db6071e07" />

<img width="701" height="251" alt="3" src="https://github.com/user-attachments/assets/b0498c3d-66fd-4838-86a3-3495150175a9" />

6. Right-click on **Anna Jones**

<img width="744" height="346" alt="4" src="https://github.com/user-attachments/assets/0d4fd874-b18d-4a54-8085-0e24d7cee6f3" />

### Disable Account
- Click **Disable Account**
- Cick **OK**

<img width="783" height="321" alt="5" src="https://github.com/user-attachments/assets/e64aafd0-2f8e-48a3-8b39-e55b22e3f64a" />

### Reset Password
- Right-click the account again the click **Reset Password**
- Enter new **password** then Click **OK**

<img width="700" height="331" alt="6" src="https://github.com/user-attachments/assets/f6597a7c-2ca2-4004-9e88-7a854c0b8d85" />

<img width="358" height="163" alt="7" src="https://github.com/user-attachments/assets/363216a0-be45-42b9-8ec0-2c463d8ad465" />

- click **OK**

### Re-enable Account

- Right-click on the user's Account then click **Enable Account**
<img width="726" height="263" alt="8" src="https://github.com/user-attachments/assets/1de11a1f-4cc0-45fd-bbfe-03ee4f44b22b" />

<img width="651" height="305" alt="9" src="https://github.com/user-attachments/assets/70e47c0e-0b66-4493-8b09-2702bcc1ceaa" />

---

## Method 2: Reset Password Using ADAC

### Steps
1. Open **Server Manager**
2. Click **Tools**
3. Click On **Active Directory Administrative Center**

<img width="936" height="596" alt="10" src="https://github.com/user-attachments/assets/a6558b35-d5f3-4c99-b91b-54d9500911f6" />

### Reset password via RESET PASSWORD Panel

- Enter username: **OTCSCORP\a.jones**
- Enter new password: ...

<img width="920" height="594" alt="11" src="https://github.com/user-attachments/assets/7e6a9827-6993-42dd-8398-98052da7a76c" />

<img width="585" height="256" alt="12" src="https://github.com/user-attachments/assets/31aee874-3f4c-492c-aa22-6d73129796f2" />

### Alternative Method
- Navigate to: **corp.local** → **Users-OU** → **Administration**
- Right-click on the user account and click **Reset Password...**

<img width="757" height="356" alt="13" src="https://github.com/user-attachments/assets/dfaa8819-f977-443f-bae5-66d3b2027c8d" />

<img width="727" height="368" alt="14" src="https://github.com/user-attachments/assets/4f67d87b-fe78-40d0-b453-f46382ac00d0" />

---

## Method 3: Reset Password Using PowerShell

### Steps

1. Search and open **Active Directory Module for Windows PowerShell**

<img width="739" height="373" alt="15" src="https://github.com/user-attachments/assets/02084fec-17f2-4606-b22f-d1853e538d19" />

<img width="815" height="424" alt="16" src="https://github.com/user-attachments/assets/02bd3724-7399-4f28-8358-f186fd2ab0bd" />

### Create Secure Password

```powershell
$password = Read-Host -AsSecureString "Enter new password"
```

This command promps for a password

<img width="750" height="276" alt="17" src="https://github.com/user-attachments/assets/cd02dcdb-054f-4b94-ada7-505a18950e4b" />

Note: **the AsSecureString does not display the password you type in plain text**

### Reset Password

```powershell
Set-ADAccountPassword -Identity "a.jones" -NewPassword $password -Reset
```

<img width="871" height="317" alt="18" src="https://github.com/user-attachments/assets/dcae72c2-6aa8-4934-bf19-5c4de1c8bcfe" />

### Force Password Change at Logon

```powershell
Set-ADUser -Identity "a.jones" -ChangePasswordAtLogon $true
```

<img width="864" height="368" alt="19" src="https://github.com/user-attachments/assets/d38bb346-33fc-4bce-b0dd-325c152f4be9" />

## Login Validation Test

<img width="753" height="529" alt="20" src="https://github.com/user-attachments/assets/b8859a67-a23e-44b7-9f49-7ca45a9475c4" />

<img width="794" height="442" alt="21" src="https://github.com/user-attachments/assets/b622bef2-a47f-4fcd-993d-330fde1d09ef" />

Anna Jones is prompted to change password at login

<img width="786" height="585" alt="22" src="https://github.com/user-attachments/assets/bb711481-709d-4ca4-828f-c2a2f4a7b5eb" />
