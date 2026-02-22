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

1. In **Server Manager**, click **Local Server**

<img width="794" height="347" alt="7" src="https://github.com/user-attachments/assets/95f7cef7-f8e2-41df-8f08-43bec0f2d5d8" />

2. Click the **Time zone**
3. Click **Change time zone**
4. Select your appropriate time zone
5. Click **OK**

<img width="429" height="247" alt="9" src="https://github.com/user-attachments/assets/cf274319-6453-45a2-9608-80e4690e7bad" />

6. Click **OK**
<img width="459" height="484" alt="10" src="https://github.com/user-attachments/assets/1208b9df-9d2b-43fa-916d-319529fea925" />

---

# Verify Security Settings  

Under **Local Server** in Server Manager:

- Ensure **Windows Defender Firewall** is **ON**

<img width="706" height="378" alt="11" src="https://github.com/user-attachments/assets/3f172ef6-3fdb-4a15-a680-790650a6b3fb" />

- Ensure **Windows Defender Antivirus** is **ON**

<img width="894" height="337" alt="12" src="https://github.com/user-attachments/assets/f0e02f9e-e047-4285-ac6c-e32c90de9dec" />

---

#  Update the Server  

## Step 3 – Install Windows Updates  

1. In **Server Manager**, click **Local Server**
2. Click **Last checked for updates**

<img width="799" height="301" alt="13" src="https://github.com/user-attachments/assets/a4847179-0314-496c-8e5d-96570625565d" />

3. Scroll down and click **Install now**
<img width="800" height="377" alt="14" src="https://github.com/user-attachments/assets/3b160191-6226-4df6-ae2f-89e4760b7d1e" />

4. Wait for updates to download and install
5. Click **Restart Now** if prompted
<img width="680" height="444" alt="15" src="https://github.com/user-attachments/assets/07676e45-c45f-4eb7-9d5a-f7cfe213a28a" />

After restart:

- Log back in
- Confirm the server shows **You're up to date**

<img width="795" height="155" alt="16" src="https://github.com/user-attachments/assets/0d31cbed-7f13-41f9-8ccc-7253e589844f" />

<img width="686" height="410" alt="17" src="https://github.com/user-attachments/assets/dab994a5-cb67-4ca5-8cd1-cc024f0bde42" />

---











