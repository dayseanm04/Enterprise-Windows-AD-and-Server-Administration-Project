# Test Password Policy GPO

Validates the settings configured in [**01-Configure-Password-Policies.md**](../../06-Security-and-Hardening/01-Account-and-Password-Policies/01-Configure-Password-Policies.md).

## Overview
With the password policy configured on the Default Domain Policy, I need to confirm it's actually being enforced. I tested using Emma Davis's account (**`e.davis`**), a test user in the HR department.

## Setup
1. Open **Active Directory Users and Computers**.
2. Expand the domain → **Users-OU** → **HR**.

<img width="686" height="383" alt="1" src="https://github.com/user-attachments/assets/2fc064e7-c5c5-4763-ac0b-5e996cc1d338" />

3. Right-click **Emma Davis**, click **Properties**.
4. On the **Account** tab, unchecked **Password never expires** and checked **User must change password at next logon**, then clicked **OK**.

<img width="644" height="546" alt="2" src="https://github.com/user-attachments/assets/fe1d4db4-052c-4c0c-80c3-972b5e54afef" />

## Test 1: Minimum Password Length
Logged in as **`e.davis`**

<img width="841" height="708" alt="3" src="https://github.com/user-attachments/assets/31658e23-2d90-41b1-ab26-24ad96e7af55" />

Was prompted to change the password at logon:

<img width="847" height="624" alt="4" src="https://github.com/user-attachments/assets/ef6bf459-442b-43d2-9791-0e4885eb375b" />

Tried the password **`bob`**, which is less than 8 characters:

<img width="811" height="649" alt="4" src="https://github.com/user-attachments/assets/b5e9dddf-931d-44e2-9358-12d0b7029c70" />

<img width="559" height="452" alt="5" src="https://github.com/user-attachments/assets/3675158e-b6bb-4921-93ac-8b341b0866b5" />

Clicked **OK** — got rejected:
