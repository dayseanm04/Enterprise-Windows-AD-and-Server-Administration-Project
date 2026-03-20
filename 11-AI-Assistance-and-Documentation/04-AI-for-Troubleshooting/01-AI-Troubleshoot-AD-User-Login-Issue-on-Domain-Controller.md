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


















