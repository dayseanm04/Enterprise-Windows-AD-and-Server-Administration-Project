# 05 - Reset Active Directory User Password Using ADUC, ADAC, and PowerShell

## Overview
This task I will demonstrate how to reset a user's password in Active Directory using multiple methods: Active Directory Users and Computers (ADUC), Active Directory Administrative Center (ADAC), and Windows PowerShell. 

---

## Objectives
- Reset a user password using ADUC
- Reset a user password using ADAC
- Reset a user password using PowerShell
- Disable and re-enable a user account
- Enforce password change at next logon

---

## Environment
- **Domain:** corp.oaktowncs.com
- **Tools Used:**
  - Active Directory Users and Computers (ADUC)
  - Active Directory Administrative Center (ADAC)
  - Active Directory Module for Windows PowerShell

---

### [Click Here for the AD User Accounts Reference](Reference-Oaktown-CS-User-Accounts.md)


### Scenario
**Anna Jones** (Administration Department) forgot her password. The goal is to reset her password using multiple methods.

---

## Method 1: Reset Password Using ADUC

### Steps
1. Open **Server Manager**
2. Click **Tools**
3. Select **Active Directory Users and Computers**
4. Clicked on the domain

<img width="747" height="344" alt="1" src="https://github.com/user-attachments/assets/d9195500-7d5d-4524-9038-ecbe7584c358" />

5. Clicked on **`Users-OU` and `Administration OU`**

<img width="899" height="361" alt="2" src="https://github.com/user-attachments/assets/2db21245-6b95-4837-adc1-0a1db6071e07" />

<img width="701" height="251" alt="3" src="https://github.com/user-attachments/assets/b0498c3d-66fd-4838-86a3-3495150175a9" />

6. Right-click on **Anna Jones**

<img width="744" height="346" alt="4" src="https://github.com/user-attachments/assets/0d4fd874-b18d-4a54-8085-0e24d7cee6f3" />

### Disable Account
- Click **Disable Account**









































