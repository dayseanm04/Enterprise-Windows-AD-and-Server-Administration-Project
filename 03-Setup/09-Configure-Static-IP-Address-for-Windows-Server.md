# 09 - Configure Static IP Address for thd Windows 2019 Server

## Overview

I will configure a **static IP address** for the **Windows Server 2019 virtual machine**.  

Assigning a static IP is critical for servers, especially **Domain Controllers**, because network services such as:
- Active Directory
- DNS
- Authentication

This server will function as the **Domain Controller** for the Oak Town Corporate Services environment.

---

# Server Information

**Server VM Name:** Windows-2019-SRV <br/>
**Server name (computer name):** OTCS-SRV-DC01 <br/>
**Role:** Domain Controller <br/>
**Network Type:** Static IP Configuration <br/>

---

# Verify Current IP Address (DHCP)

Before configuring a static IP, I verified the current network configuration.

### Step 1

Open **Command Prompt**.

### Step 2

Run the following command:

```bash
ipconfig /all
```

### Result

<img width="900" height="485" alt="30" src="https://github.com/user-attachments/assets/090da12a-623b-4f56-ac22-9e5e206beb86" />

Note: The server initially received this **IP address from DHCP**, I using the Hyper-V default switch.

---

# Configure Static IP Address

### Step 1

Open **Control Panel**.

<img width="793" height="353" alt="31" src="https://github.com/user-attachments/assets/1055d9ed-bf67-4197-9bf8-3546f9dd124c" />

---

### Step 2

Click on **Network and Internet**

<img width="806" height="299" alt="32" src="https://github.com/user-attachments/assets/fa18184a-996b-4d29-8586-5c4a7d2b1efc" />

---

### Step 3

Click on **Network and Sharing Center**

<img width="783" height="339" alt="33" src="https://github.com/user-attachments/assets/08d902f5-d443-484d-9af2-1018da89eb3f" />

---

### Step 4

Click the active network adapter: **Ethernet**

<img width="577" height="451" alt="34" src="https://github.com/user-attachments/assets/5b1bed2d-85bb-4ad1-8bc7-c45afd8be940" />

---

### Step 5

Click on **Properties**

<img width="606" height="505" alt="35" src="https://github.com/user-attachments/assets/63d12ed4-6e82-4340-bb5d-77a4e163e4b3" />

- Select **Internet Protocol Version 4 (TCP/IPv4)**
- Then click **Properties**.

<img width="692" height="518" alt="36" src="https://github.com/user-attachments/assets/4ab8b92a-756e-415d-8e37-3b3fe6c98a7f" />




















