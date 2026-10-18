# Enterprise Windows AD and Server Administration Project

<img width="636" height="283" alt="Active-Directory" src="https://github.com/user-attachments/assets/c920a2bd-240f-4f62-a593-86ee63ad80b8" />

## Overview
In this project I designed, deployed, and administered a Windows Server 2019 domain environment for a simulated company, **Oak Town Corporate Services**. Everything runs on Hyper-V on my own machine.

The goal was to do the work a real sysadmin does: build the server, set up Active Directory and DNS, organize users and computers, lock down accounts with Group Policy, automate repetitive tasks with PowerShell, and then test and troubleshoot everything I built. Every step is documented with screenshots.

## The Company

Oak Town Corporate Services is a small-to-medium business in one building with two floors and five departments.

| Department | Employees |
|------------|-----------|
| Finance | 5 |
| Human Resources | 5 |
| Administration | 5 |
| IT | 3 |
| Customer Service | 2 |

**Domain:** `corp.oaktowncs.com`

## Environment

- **Hypervisor:** Microsoft Hyper-V
- **Server:** Windows Server 2019 (Domain Controller + DNS)
- **Client:** Windows 11 joined to the domain
- **Networking:** Hyper-V virtual switches, static IP on the server
- **Test environment:** cloned production server on an internal virtual switch

## What I Built

### Server Setup

- Enabled Hyper-V and created storage and ISO folders with PowerShell
- Built and deployed the Windows Server 2019 VM
- Completed post-install configuration, virtual switch setup, and static IP

### Active Directory
- Installed AD DS and promoted the server to a Domain Controller
- Designed and built an OU structure split by **Users, Workstations, Groups, Servers, and Disabled Objects**, with department sub-OUs (IT split into Admins and Standard)
- Created users for each department and role-based security groups
- Enabled the AD Recycle Bin
- Reset passwords using ADUC, ADAC, and PowerShell
- Joined a Windows 11 computer to the domain

### DNS
- Configured forward and reverse lookup zones
- Created A and PTR records
- Validated name resolution both ways

### Security and Group Policy













































