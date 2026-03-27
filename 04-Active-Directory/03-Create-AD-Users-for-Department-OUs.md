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
- Default password: `ChangeMe10@`
- Company: OakTown Corporate Services

### Example

<img width="905" height="531" alt="3" src="https://github.com/user-attachments/assets/3deba644-be60-45e7-b84b-0e4610fc1562" />

### Verify AD User Accounts creation

<img width="821" height="361" alt="4" src="https://github.com/user-attachments/assets/8837f2d2-6f68-4a3e-ae44-ca9651a7f3e4" />

<img width="802" height="375" alt="5" src="https://github.com/user-attachments/assets/1d300608-dde7-46a6-ac4d-73c64ce157cb" />

<img width="876" height="376" alt="6" src="https://github.com/user-attachments/assets/f1a799c6-ea1e-4f07-b86f-b2f19e44d0a3" />

<img width="802" height="402" alt="7" src="https://github.com/user-attachments/assets/80278f83-2c70-4b3a-bf9e-9580a6f4b77b" />



## User Accounts Table

| Department          | Name           | Account Type | Logon Name        | Notes                   |
|--------------------|----------------|--------------|-------------------|--------------------------|
| Administration     | Michael Brown  | Standard     | corp\m.brown      |                          |
| Administration     | Anna Jones     | Standard     | corp\a.jones      |                          |
| Customer Service   | James Wilson   | Standard     | corp\j.wilson     |                          |
| Customer Service   | Sarah Miller   | Standard     | corp\s.miller     |                          |
| HR Department      | Robert Taylor  | Standard     | corp\r.taylor     |                           |
| HR Department      | Emma Davis     | Standard     | corp\e.davis      |                           |
| Finance            | David Clark    | Standard     | corp\d.clark      |                           |
| Finance            | Laura White    | Standard     | corp\l.white      |                           |
| IT Department      | Daniel Moore   | Admin        | corp\d.moree      | System Administrator      |
| IT Department      | Daniel Moore   | Standard     | corp\da.moree     | IT Support                |
| IT Department      | Sophie Hall    | Admin        | corp\s.hall       | System Administrator      |
| IT Department      | Sophie Hall    | Standard     | corp\so.hall      | IT Support                |



























