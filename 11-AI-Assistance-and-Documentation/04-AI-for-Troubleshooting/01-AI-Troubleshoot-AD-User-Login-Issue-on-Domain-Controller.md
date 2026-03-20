# 01 AI Troubleshoot AD User Login Issues on Domain Controller

## Overview
This document demonstrates how I google gemini to troubleshoot and resolve an Active Directory (AD) user login issue on a Domain Controller. 

---

## Objective
- Troubleshoot a user login failure on a Domain Controller  
- Identify the root cause of the issue  
- Document how AI assisted in the troubleshooting process  

---

## Problem Description
A newly created Active Directory user account was unable to log in to the Domain Controller.

### Error Observed
"The sign-in method you're trying to use isn't allowed. for more info, contact your network administrator"


<img width="598" height="435" alt="36" src="https://github.com/user-attachments/assets/75de62f6-63fd-4f2b-b9aa-1afd5918a6cd" />

---

## Root Cause Analysis
Based on the error message and system behavior, the issue was identified as:

- The user did not have sufficient privileges to log into a Domain Controller  
- Domain Controllers enforce strict security policies  
- Only privileged users (such as members of the Domain Admins group) are allowed to log in locally by default

---

## AI Assistance Used

### After I created a user account in active directory and I tried to login using that account I got this message "This sign-in method you're trying to use isn't allowed. For more info, contact your network administrator".


### AI Guidance
- Explained that Domain Controllers have restricted login policies  
- Clarified that standard users do not have permission to log in locally  
- Suggested verifying group membership and user rights assignments  

---

## Troubleshooting Steps

1. Open **Active Directory Users and Computers**
2. Expand domain
3. Clicked **Users**

<img width="1015" height="624" alt="TS20" src="https://github.com/user-attachments/assets/979c41df-0011-43f9-8722-87063ec1f494" />

4. Right clicked **Domain Users**
5. Clicked **properties**
6. Click **member**

<img width="706" height="588" alt="TS21" src="https://github.com/user-attachments/assets/6b2cb757-5bd0-4e2e-bb6b-389eeefbde5c" />

Note: that john doe is part of the Domain Users group. Click OK

1. Right click **Domain Admins**
2. Click **properties**
3. Click **member**

<img width="725" height="567" alt="TS22" src="https://github.com/user-attachments/assets/d1b85979-6312-463b-b0dc-0d5d66ab19df" />

Note: Only Administrator is appart of the Domain Admins group that is whay Im able to log into the Domain Controller as Administrator.

### Fix

1. Click **Add**
2. Under Enter object names to select
3. Type **john doe** and Check Name
4. Click **OK**

<img width="787" height="493" alt="TS23" src="https://github.com/user-attachments/assets/ce93d19b-2b73-4326-933e-bde96c43bb52" />

5. Click **OK**

<img width="724" height="670" alt="TS24" src="https://github.com/user-attachments/assets/12561d53-caf8-47d4-9dbb-c8894836ba3e" />

### Attempt login

I will attempt to log in as john doe

<img width="824" height="700" alt="TS25" src="https://github.com/user-attachments/assets/5d9c2773-5e42-4b2e-a48b-e6e46e0f8134" />

I successfully logged in as john doe

### Verification

1. Open PowerShell
2. net user



