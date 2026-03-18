# 01 – Test PowerShell Script to Create AD User Accounts

## Overview

I will test the PowerShell script generated using AI to automate the creation of Active Directory user accounts.

The goal of this test was to:

- Validate that the script successfully creates user accounts  
- Review the accounts it created  
- Confirm login for the created users  

---

 Find the script [**here**](https://github.com/dayseanm04/Enterprise-Windows-AD-and-Server-Administration-Project/blob/main/11-AI-Assistance-and-Documentation/03-AI-Generated-Scripts/01-Create-AD-Users-Account-Script.md)

## Test Environment

- Server: TST-AD-SRV  
- Domain: corp.oaktowncs.com  

## Save and Run the Script

I copied the script and pasted in in Powershell ISE scrip pane. I ran ran that scriped and saved it in a folder in my Desktop

### Result

- User accounts were successfully created  
- Accounts appeared under the correct OUs in **Active Directory Users and Computers**  

<img width="685" height="381" alt="1" src="https://github.com/user-attachments/assets/a2b8f6ac-06a5-4e06-84c8-e4de7e567baf" />

<img width="739" height="482" alt="2" src="https://github.com/user-attachments/assets/037b100d-b853-4373-b9e2-30eb63da317b" />

## Issue Identified

When I first ran this script I didn't make any changes to the script. It created the user accounts. 

But I didn't change **company** to **oaktowncs**, note that the actual domain name is **corp.oaktowncs.com**. When I used AI to generate the script I didn't include the actual domain name I used **corp.company.com**.

After reviewing the created accounts:

### Problem 1 – Incorrect Domain in UPN

#### Review HR user accounts

- Expand on corp.oaktowncs.com
- Click on Users-OU
- Click on HR
- Right click on HR-User1
- Click properties
- Click on account

<img width="408" height="542" alt="3" src="https://github.com/user-attachments/assets/0b504888-b2f6-41ed-ab22-6f7730d43b42" />

User accounts were created with: **@corp.company.com** instead of: **@corp.oaktowncs.com**

### Problem 2 – Inconsistent Username Formatting

- Some usernames contained inconsistent formatting  
- Example: spaces 

<img width="404" height="538" alt="4" src="https://github.com/user-attachments/assets/7c24b807-4bd6-45d0-bd11-4287fcfb2479" />

### Fix 1 – Update Domain in Script

Clicked on domain name and change it to corp.oaktowncs.com
Changeed user logon name to hruser1
Clicked OK

<img width="703" height="542" alt="5" src="https://github.com/user-attachments/assets/4f27dd52-0e89-4018-92b5-cdebcb77e907" />





















