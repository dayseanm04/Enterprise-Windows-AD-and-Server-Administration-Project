# 02 – Configure Hyper-V Internal Virtual Switch for Test Environment

## Overview

To prevent interference with the production network, the test server environment will be connected to an **isolated internal virtual network**.

I will create an **Internal Virtual Switch** in Hyper-V and connecet the TST-AD-SRV VM to it. This allows communication between the host and the TST-AD-SRV VM while keeping the testing environment separated from the production network.

This configuration ensures that testing Active Directory changes or system configurations will **not impact the production server environment**.

---

### Step 1 – Open Hyper-V Manager

1. Open **Hyper-V Manager**
2. In the right-hand **Actions** panel, click **Virtual Switch Manager**

<img width="1021" height="325" alt="1" src="https://github.com/user-attachments/assets/16e557cb-a17c-49e5-a5e8-598dbd1bbd19" />

---

### Step 2 – Create Internal Virtual Switch

Inside **Virtual Switch Manager**:
1. Select **Internal**
2. Click **Create Virtual Switch**

<img width="736" height="291" alt="2" src="https://github.com/user-attachments/assets/9ab6287f-6adb-4d27-923a-36588e2df3f7" />

Configured the switch with the following settings:<br/>
Virtual Switch Name: **OTCS-TEST-SW**<br/>
Notes: **Notes**<br/>

Click **OK** to create the switch.

<img width="728" height="382" alt="3" src="https://github.com/user-attachments/assets/097edba1-fd62-4ccb-bb0f-dbcf5041b6ab" />

---

### Step 3 – Configure TST-AD-SRV to use OTCS-TEST-SW

1. In **Hyper-V Manager**
2. Right-click on **TST-AD-SRV**
3. Click **Settings**

<img width="1021" height="325" alt="1" src="https://github.com/user-attachments/assets/16e557cb-a17c-49e5-a5e8-598dbd1bbd19" />














