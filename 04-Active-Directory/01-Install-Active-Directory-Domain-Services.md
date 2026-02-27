# 01 – Install Active Directory Domain Services (AD DS)

## Overview

In this phase I will deploy Active Directory Domain Services (AD DS) and promotes the Windows Server 2019 VM to a Domain Controller.

During this process:

- I will install AD DS role on the Windows-2019-SRV VM
- Create a new forest
- Configure a root domain
- Promoted to a Domain Controller
- Scan Best Practices Analyzer(BPA) after AD DS installation

---

# Environment Details

- **Company Name:** Oak Town Corporate Services
- **Forest Root Domain:** corp.oaktowncs.com
- **NetBIOS Domain Name:** OTCSCORP
- **Server Role:** Domain Controller (DC01)

---

# Step 1 – Install AD DS Role

1. Open **Server Manager**
2. Click **Manage** (top-right)
3. Select **Add Roles and Features**

<img width="397" height="209" alt="1" src="https://github.com/user-attachments/assets/b2e1a784-71ec-4da1-a4c8-0e08ce0c4e1a" />

