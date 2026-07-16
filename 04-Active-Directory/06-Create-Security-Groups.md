# Creating Security Groups in Active Directory

## Overview
In this task I will create Security Groups for each department within Active Directory using the Active Directory Users and Computers (ADUC) console.

## Objectives
Create departmental security groups to manage resource permissions

## Steps to Create Security Groups

### 1. Open Active Directory Users and Computers
- Open Server Manager
- Click Tools
- Select Active Directory Users and Computers

<img width="588" height="246" alt="11" src="https://github.com/user-attachments/assets/e7215b94-1ca4-4139-8e01-b704dede3258" />

### 2. Navigate to Security-Group-OU
- Expand corp **corp.oaktowncs.com**
- Expand **Groups-OU**
- Click on **Security-Group-OU**

<img width="622" height="329" alt="3" src="https://github.com/user-attachments/assets/450382d9-e5ab-45c8-9160-66a95ac34c2b" />

### 3. Create Security Groups
- Right click any empty space
- Click **New**
- Click **Group**

<img width="658" height="402" alt="4" src="https://github.com/user-attachments/assets/e0a06436-2e02-4e5a-aaa4-fda68f8d4fdb" />

### Enter group details:
- Group name (e.g., **Administration-Sec-Group**)
- Group scope: Select **Global**
- Group type: Select **Security**
- Click **OK**

## Naming Convention
Security group names follow this format:
### [Department Name] + -Sec-Group

## Reference Security Groups

<img width="622" height="329" alt="3" src="https://github.com/user-attachments/assets/450382d9-e5ab-45c8-9160-66a95ac34c2b" />

