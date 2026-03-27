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

<img width="773" height="683" alt="10" src="https://github.com/user-attachments/assets/fcb8434c-878a-4257-81ba-41266c5fe018" />

<img width="861" height="518" alt="11" src="https://github.com/user-attachments/assets/658bc172-1558-403b-a80e-a9769bcd68ff" />

<img width="811" height="437" alt="12" src="https://github.com/user-attachments/assets/ec97d389-2790-46f1-9cf8-9f8b6a91a8ab" />

**Result:**
- Login attempt failed on the domain controller















