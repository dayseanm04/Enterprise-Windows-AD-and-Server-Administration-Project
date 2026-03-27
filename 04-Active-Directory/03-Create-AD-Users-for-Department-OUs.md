# 03 - Create AD Users for Department OUs

## Reference OU Design

<img width="757" height="398" alt="01-OU-Design-Workstations-and-Users" src="https://github.com/user-attachments/assets/a66653fe-5ce8-4939-aecd-bc09d57ef767" />

## Overview
In this task I will create and organize user accounts within department Organizational Units (OUs) in Active Directory using the Active Directory Administrative Center (ADAC). 

---

## Objectives
- Create user accounts for multiple departments

---

## Steps to Create Users

### 1. Open Active Directory Administrative Center
- Open **Server Manager**
- Click **Tools**
- Select **Active Directory Administrative Center**

### 2. Navigate to Users OU
- Expand `corp (local)`
- Select **Users-OU**

<img width="935" height="379" alt="1" src="https://github.com/user-attachments/assets/c8727afc-82e6-4357-ab80-3494b552a4fa" />

---

### 3. Create Users in Department OUs
- Select a department OU (e.g., **Administration**)
- Right-click inside the OU,
- Click **New**
- Click **User**

<img width="436" height="140" alt="2" src="https://github.com/user-attachments/assets/b289adf9-e9ba-444f-9aba-7f457714b1b3" />

- Enter user details:
  - First Name
  - Last Name
  - User logon name

---

## Naming Convention
User logon names follow this format:

first initial + last name (regular accounts)

---

### Account Configuration Settings

The following settings were applied during user creation:

- User must change password at next logon
- Account expiration set to never
- Protect object from accidental deletion enabled


































