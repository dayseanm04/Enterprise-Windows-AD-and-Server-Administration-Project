# 02 – Implement Active Directory OU Structure

## Overview

This phase I implemented the **Organizational Unit (OU) structure** for the Active Directory environment of **Oak Town Corporate Services**.

View the: [OU Design](/02-Design/OU-Designs/03-Design-Organizational-Unit-Structure.md)

## Reference OU Design

<img width="757" height="398" alt="01-OU-Design-Workstations-and-Users" src="https://github.com/user-attachments/assets/a66653fe-5ce8-4939-aecd-bc09d57ef767" />

<img width="932" height="315" alt="02-OU-Design-Groups-and-Servers" src="https://github.com/user-attachments/assets/2fb7d178-db0d-4772-a4c2-1bce6055ab8e" />

The domain used in this environment is: **corp.oaktowncs.com**

---

### Step 1 – Open Active Directory Users and Computers

1. Open **Server Manager**
2. Click **Tools**
3. Select **Active Directory Users and Computers**

<img width="590" height="196" alt="40" src="https://github.com/user-attachments/assets/44f373f3-d212-41a3-8960-505940cca50d" />

### Step 2 – Create Core Organizational Units

Expand the domain **corp.oaktowncs.com**

<img width="757" height="269" alt="41" src="https://github.com/user-attachments/assets/a645776a-fdda-4e2e-84b9-58bd5f299f15" />

Right-click the domain and select: New > Organizational Unit


Create the following OUs:

- Users-OU
- Workstations-OU
- Groups-OU
- Servers-OU
- Disabled-OU

Enable the option: **Protect container from accidental deletion**
