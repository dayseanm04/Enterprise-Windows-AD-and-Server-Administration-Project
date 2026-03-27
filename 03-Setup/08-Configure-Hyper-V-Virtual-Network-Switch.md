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
- **Description:** Virtual switch for windows AD and Server administration
- **Connection Type:** External network
- Select the appropriate **physical network adapter**

<img width="724" height="550" alt="32" src="https://github.com/user-attachments/assets/3572c2cc-3439-4e78-8272-2a31461810a2" />

5. Click **Apply**
6. Click **Yes** if prompted about network interruption
7. Click **OK**

<img width="360" height="251" alt="33" src="https://github.com/user-attachments/assets/ad619a66-897c-4be3-930a-ef1b4b68d29c" />

---

# Step 2 – Attach the Virtual Switch to the VM

1. In **Hyper-V Manager**
2. Right-click the **Windows-2019-SRV** virtual machine
3. Click **Settings**

<img width="462" height="135" alt="34" src="https://github.com/user-attachments/assets/6e1bff51-796f-4462-be24-ab36dad32026" />

4. Click on **Network Adapter**
5. Under **Virtual Switch**, select: **`OTCS-SW`**
6. Click **Apply**
7. Click **OK**

<img width="725" height="358" alt="35" src="https://github.com/user-attachments/assets/44fc9902-a3e2-42fa-be98-efbbdaadd06d" />

---

# Step 3 – Verify Network Connectivity

1. Start the **Windows-2019-SRV** virtual machine
2. Log in
3. Open **Command Prompt**
4. Run: **`ipconfig`**

<img width="715" height="311" alt="37" src="https://github.com/user-attachments/assets/2efffeeb-f54c-4780-8e0d-6a5f30f54eba" />

### Test Connectivity to Host Machine

ping 192.168.1.151

<img width="501" height="290" alt="38" src="https://github.com/user-attachments/assets/5ba29111-eb41-4635-bc6a-ddd55f9dc4d1" />
