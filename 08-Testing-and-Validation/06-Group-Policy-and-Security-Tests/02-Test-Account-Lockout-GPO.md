# Test Account Lockout Policy

Validates the settings configured in [**02-Configure-Account-Lockout-Policies.md**](../../06-Security-and-Hardening/01-Account-and-Password-Policies/02-Configure-Account-Lockout-Policies.md).

## Overview
With the account lockout policy configured on the Default Domain Policy, I tested it to confirm accounts actually lock out after repeated failed logins,  and that the "Allow Administrator account lockout" setting also applies to the built-in Administrator account.

## Test 1: Invalid Login Attempts (Lockout Threshold)
Logged in as **`e.davis`** with an incorrect password, 5 times in a row.

<img width="729" height="497" alt="1" src="https://github.com/user-attachments/assets/430373f2-fb58-47af-9267-7bb33a15cd7e" />

<img width="590" height="408" alt="2" src="https://github.com/user-attachments/assets/86e8613e-e5f0-4a32-a946-7bf6475d2081" />

<img width="958" height="742" alt="3" src="https://github.com/user-attachments/assets/a47cc39a-e349-4655-ba57-437ba741f8d0" />

**Result:** The 5 invalid login attempts threshold was enforced correctly.
