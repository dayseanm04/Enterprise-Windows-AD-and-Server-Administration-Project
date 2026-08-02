# Test Password Policy GPO

Validates the settings configured in [**01-Configure-Password-Policies.md**](../../06-Security-and-Hardening/01-Account-and-Password-Policies/01-Configure-Password-Policies.md).

## Overview
With the password policy configured on the Default Domain Policy, I need to confirm it's actually being enforced. I tested using Emma Davis's account (**`e.davis`**), a test user in the HR department.

## Setup
1. Open **Active Directory Users and Computers**.
2. Expand the domain → **Users-OU** → **HR**.

<img width="686" height="383" alt="10" src="https://github.com/user-attachments/assets/2fc064e7-c5c5-4763-ac0b-5e996cc1d338" />

3. Right-click **Emma Davis**, click **Properties**.
4. On the **Account** tab, unchecked **Password never expires** and checked **User must change password at next logon**, then clicked **OK**.

