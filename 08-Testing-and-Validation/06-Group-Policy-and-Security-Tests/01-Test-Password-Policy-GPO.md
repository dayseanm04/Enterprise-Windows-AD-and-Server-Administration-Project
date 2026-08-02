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
Logged in as **`e.davis`** and was prompted to change the password at logon:

<img width="841" height="708" alt="12" src="https://github.com/user-attachments/assets/31658e23-2d90-41b1-ab26-24ad96e7af55" />
