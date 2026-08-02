# Test Account Lockout Policy

Validates the settings configured in [**02-Configure-Account-Lockout-Policies.md**](../../06-Security-and-Hardening/01-Account-and-Password-Policies/02-Configure-Account-Lockout-Policies.md).

## Overview
With the account lockout policy configured on the Default Domain Policy, I tested it to confirm accounts actually lock out after repeated failed logins,  and that the "Allow Administrator account lockout" setting also applies to the built-in Administrator account.

## Test 1: Invalid Login Attempts (Lockout Threshold)
Logged in as **`e.davis`** with an incorrect password, 5 times in a row.
