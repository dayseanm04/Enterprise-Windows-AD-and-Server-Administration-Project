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

### Role Installation Wizard

1. Click **Next** in the before you begin page
2. Select:
   - **Role-based or feature-based installation**
3. Click **Next**

<img width="792" height="310" alt="2" src="https://github.com/user-attachments/assets/54d72dba-648a-468e-9346-488dbebaf0ef" />

4. Select the local server
5. Click **Next**

<img width="774" height="355" alt="3" src="https://github.com/user-attachments/assets/7a653677-8c90-4972-b28f-f5e723dc89f5" />

6. Select:
   - **Active Directory Domain Services**

<img width="582" height="215" alt="4" src="https://github.com/user-attachments/assets/295b20bb-de7e-4665-88e8-56543d7125c7" />

7. Click **Add Features**
make sure **`Include management tools (if applicable)`** is checked

<img width="416" height="424" alt="5" src="https://github.com/user-attachments/assets/2503a21a-c310-4f46-af65-fb0cb54fc4a4" />

8. Click **Next**
9. Click **Next**

<img width="788" height="557" alt="6" src="https://github.com/user-attachments/assets/67059d6a-1166-404c-b86e-596fa8a9dac9" />

10. Check:
    - ✅ Restart the destination server automatically if required

<img width="785" height="398" alt="7" src="https://github.com/user-attachments/assets/8cf87907-80f1-4586-aec1-93b2600869f0" />



