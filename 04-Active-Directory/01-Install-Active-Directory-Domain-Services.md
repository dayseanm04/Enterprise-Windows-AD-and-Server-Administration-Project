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

11. Click **Yes** at the confirmation page
12. Click **Install**

<img width="782" height="560" alt="8" src="https://github.com/user-attachments/assets/389da9fc-a027-4576-adcd-4556cf06041b" />

Wait for installation to complete.

# Step 2 – Promote Server to Domain Controller

After installation completes:

1. Click **Promote this server to a domain controller**

<img width="592" height="463" alt="9" src="https://github.com/user-attachments/assets/a59005e9-471d-4bce-8853-26236cb48204" />

### Deployment Configuration

1. Select:
   - **Add a new forest**
2. Enter Root Domain Name: corp.oaktowncs.com

<img width="762" height="338" alt="10" src="https://github.com/user-attachments/assets/5e281307-18b9-4e5f-9ff7-d8795e7257b5" />

3. Click **Next**

# Step 3 – Domain Controller Options

1. Set the **Directory Services Restore Mode (DSRM) password**
2. Click **Next**

<img width="755" height="558" alt="11" src="https://github.com/user-attachments/assets/1cf8d3da-ad47-4daf-b264-af61cff3bf7b" />

# Step 4 – DNS Options

1. Ensure that **Create DNS delegation** is unchecked
2. Click **Next**

<img width="764" height="567" alt="12" src="https://github.com/user-attachments/assets/49ff7cfc-e50f-4e32-9043-350fee95ebd6" />

---

# 5 Step 5 – NetBIOS Domain Name

The system auto-generates:

1. NETBIOS name: **`OTCSCORP`**
2. Click **Next**

<img width="756" height="558" alt="13" src="https://github.com/user-attachments/assets/7bbc3e39-60ff-4158-a98d-95066891b752" />

#  Step 6 – Additional Configuration

1. Click **Next** under the paths page

<img width="761" height="562" alt="14" src="https://github.com/user-attachments/assets/8a6f9554-37f0-487c-93a1-260f1a1424d2" />

2. Click **Install**

<img width="759" height="558" alt="15" src="https://github.com/user-attachments/assets/bace250f-2ef9-4fc3-904b-9ccbbf25656c" />












