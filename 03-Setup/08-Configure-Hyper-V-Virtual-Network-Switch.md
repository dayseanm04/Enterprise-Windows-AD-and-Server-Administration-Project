# 08 – Configure Hyper-V Virtual Network Switch

## Overview

In order for the Windows Server 2019 virtual machine to communicate with the physical network and my host machince, I have to configure an external Virtual Switch in Hyper-V.

---

# Step 1 – Create an External Virtual Switch

1. Open **Hyper-V Manager**
2. On the right panel, click **Virtual Switch Manager**

<img width="425" height="142" alt="30" src="https://github.com/user-attachments/assets/ad7e3e5a-08fa-4e6f-802a-205590f643e2" />

4. Select **External**
5. Click **Create Virtual Switch**

<img width="725" height="281" alt="31" src="https://github.com/user-attachments/assets/fcac793a-9707-48d0-a515-1b8d4c90539c" />

### Configuration:

- **Name:** `OTCS-SW`
- **Description:** Virtual switch for Oak Town Corporate Services AD Lab
- **Connection Type:** External network
- Select the appropriate **physical network adapter**

<img width="724" height="550" alt="32" src="https://github.com/user-attachments/assets/3572c2cc-3439-4e78-8272-2a31461810a2" />

5. Click **Apply**
6. Click **Yes** if prompted about network interruption
7. Click **OK**

<img width="360" height="251" alt="33" src="https://github.com/user-attachments/assets/ad619a66-897c-4be3-930a-ef1b4b68d29c" />



