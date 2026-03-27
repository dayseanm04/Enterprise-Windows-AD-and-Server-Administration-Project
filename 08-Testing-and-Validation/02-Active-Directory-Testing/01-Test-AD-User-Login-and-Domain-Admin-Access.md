# 01 - Test AD User Login and Domain Admin Access

## Overview

I will login to a AD user accounts I created. This test validates Active Directory user authentication. It includes logging in with a standard user account, verifying access restrictions on the domain controller (**OTCS-SRV-DC01**), assigning Domain Admin privileges, and verifying successful login.

---


## Objectives
- Test login with a standard AD user account
- Identify domain controller login restrictions
- Assign Domain Admin privileges to a user
- Validate successful administrative login

---


## Environment
- **Domain:** corp.oaktowncs.com
- **Tools Used:**
  - Active Directory Users and Computers (ADUC)
  - Windows Server (Domain Controller)

---

## Test Scenario

### 1. Attempt Login with Standard User

- Username: **`m.brown`**
- Password: **`ChangeMe10@`**

Prompted me to changed the password because I specified change password at the next log on

<img width="773" height="683" alt="1" src="https://github.com/user-attachments/assets/fcb8434c-878a-4257-81ba-41266c5fe018" />

<img width="861" height="518" alt="2" src="https://github.com/user-attachments/assets/658bc172-1558-403b-a80e-a9769bcd68ff" />

<img width="811" height="437" alt="3" src="https://github.com/user-attachments/assets/ec97d389-2790-46f1-9cf8-9f8b6a91a8ab" />

**Result:**
- Login attempt failed on the domain controller

**Reason:**
- Only members of privileged groups (e.g., Domain Admins or Administrator) are allowed to log in to a domain controller

---

### 2. Identify the Issue
- The error message indicates that the sign-in method is not allowed
- This confirms restricted access for non-admin users on domain controllers

---

## Fix: Assign Domain Admin Privileges

I will assign **Daniel Moore** as a the Domain Admin G


### 3. Open Active Directory Users and Computers
- Open **Server Manager**
- Click **Tools**
- Select **Active Directory Users and Computers**
- Clicked on the **Domain**

<img width="760" height="351" alt="4" src="https://github.com/user-attachments/assets/44a08b5a-c670-4e1c-a236-710c81ea7643" />

---

### 4. Add User to Domain Admins Group
- Double Clicked on **`Users`**

<img width="1004" height="403" alt="5" src="https://github.com/user-attachments/assets/babbab2e-e95e-41d8-938f-bb2db768bb4f" />

- Clicked on the **Members** tab

<img width="726" height="458" alt="6" src="https://github.com/user-attachments/assets/e95d7b48-d619-464d-ae1b-edbe72cf18e2" />
- Click **Add**

---

### 5. Add Daniel Moore to Domain Admins
- Click **Add**

<img width="673" height="409" alt="7" src="https://github.com/user-attachments/assets/8e1288b0-c898-4e4a-b9ba-0e90b7ccec6a" />

- Entered: **`daniel`** under **Enter the object names to select**
- Clicked **Check Names**

<img width="882" height="444" alt="8" src="https://github.com/user-attachments/assets/d1543c2a-c7a5-4a48-a9cf-5f69c6ca891a" />

- Select the **admin account (d.moore)**
- Click **OK**

<img width="680" height="328" alt="9" src="https://github.com/user-attachments/assets/bf561895-0e38-4ec5-b051-6607f3d7418c" />

- Click **OK**

<img width="706" height="452" alt="10" src="https://github.com/user-attachments/assets/425429c9-657d-42df-856a-83e6a2e04806" />

















































