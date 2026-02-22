# 06-Post Installation Server Configuration

## Overview  

After deploying Windows Server 2019, several I completeed severale post-installation tasks.

This phase ensures the server:

- Has a hostname and description  
- Uses the correct time zone  
- Has security features enabled  
- Is fully updated  

This prepares the server for Active Directory Domain Services (AD DS) deployment.

---

# Configure Server Identity  

## Step 1 – Rename the Server  

1. Open **Server Manager**
2. Click **Local Server**
3. Click the current computer name
4. Select **Change**

<img width="714" height="230" alt="1" src="https://github.com/user-attachments/assets/c26dd9a8-e2db-4801-8422-6e262ad32571" />

- **Computer Description:**  Oak Town Corporate Services - ADS
<img width="410" height="290" alt="2" src="https://github.com/user-attachments/assets/b05872da-bce2-406d-8cce-02e0a3873c8a" />

- **Computer Name:**  OTCS-SRV-DC01

<img width="334" height="402" alt="3" src="https://github.com/user-attachments/assets/8a8409d3-f7f9-4e21-bbcb-209f972e6f96" />

5. Click **OK**

<img width="764" height="492" alt="4" src="https://github.com/user-attachments/assets/3d7fd903-d025-405d-9a1d-0293a6dbfff4" />

6. Click **OK** for Before restarting ...
7. Click **Apply**

<img width="410" height="474" alt="5" src="https://github.com/user-attachments/assets/9c726dbe-0ff3-4314-b366-471db8cda164" />

8. Click **Restart Now**

<img width="354" height="172" alt="6" src="https://github.com/user-attachments/assets/3592c9af-a3d5-4737-98ff-a1b0a08ae237" />

After restart, log back in to continue configuration.

---

# Configure Time Settings  

## Step 2 – Set Time Zone  





