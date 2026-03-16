# 01 – Clone Production Server to Create Test Environment

## Overview

Before implementing changes in the production Active Directory environment, I will create a **test environment** to safely validate configurations and administrative tasks.

In this phase, I will the **export and import** production server virtual machine using Hyper-V. The cloned virtual machine serves as a **test Server / Domain controller** where changes can be evaluated before applying them to the production server.

---

## Environment Context

Production Server VM: **Windows-2019-SRV**

Test Server VM: **TST-AD-SRV**

The test server will be used for:

- Configuration testing
- Active Directory experiments
- Group Policy validation
- Administrative tasks testing
- Automation tests

---

### Step 1 – Create Export Folder for VM

Open **PowerShell** and create a directory where the exported virtual machine will be stored.

Navigate to the Desktop:

```powershell
cd Desktop
```

Create the export folder:

```powershell
mkdir SRV2019_Export
```

This folder will store the exported VM files.

<img width="712" height="400" alt="1" src="https://github.com/user-attachments/assets/afbbef0a-03d1-4255-bdf4-68d0cca70674" />

### Step 2 – Create VHD Folder for Test Server

Create a folder to store the virtual hard disk for the cloned server.

Navigate to the C drive:

```powershell
cd C:\
```

Create the VHD directory:

```powershell
mkdir TestWinSRV2019-VHD
```

This folder will store the virtual hard disk files for the test server..

<img width="824" height="399" alt="2" src="https://github.com/user-attachments/assets/670b911b-23be-4690-8282-29e470c19632" />

### Step 3 – Export Production Virtual Machine

Open Hyper-V Manager.

1. Right click on **Windows-2019-SRV**

<img width="767" height="350" alt="3" src="https://github.com/user-attachments/assets/8640ced4-632d-431a-9075-511f395f3d48" />

2. Click on **Export..**
3. Browse to the export folder (**SRV2019_Export**) created earlier:

<img width="481" height="160" alt="4" src="https://github.com/user-attachments/assets/668a6083-2e00-4dea-8df2-202269ded162" />


4. Click **Export**

<img width="695" height="300" alt="5" src="https://github.com/user-attachments/assets/baebde5a-e2fb-40a1-afc5-3b9b1e307772" />

Export completed

### Step 4 – Import the Virtual Machine

After the export completes, import the virtual machine.

In Hyper-V Manager 

1. Click **Import Virtual Machine**

<img width="741" height="286" alt="6" src="https://github.com/user-attachments/assets/e0db6320-e78d-4c8f-b4f7-4ed908e11b83" />

2. Click **Next**
3. Browse to the exported VM folder **SRV2019_Export**
4. Select the exported virtual machine and click **Next**.

<img width="692" height="235" alt="7" src="https://github.com/user-attachments/assets/d7543203-c5bc-45c0-a7e9-a8539bf15e88" />

5. Select the exported virtual machine and click **Next**.

<img width="711" height="284" alt="8" src="https://github.com/user-attachments/assets/621965aa-6551-4904-9924-43d88a923bc0" />

6. Select **Copy the virtual machine (create a new unique ID)** and click **Next**.

<img width="617" height="244" alt="9" src="https://github.com/user-attachments/assets/3db78012-3dfc-4d26-99fb-5e16723dd327" />

7. In the **Choose Destination** click **Next** section click ****

<img width="705" height="526" alt="10" src="https://github.com/user-attachments/assets/29b50594-aa51-4d7a-8e2f-9def30749b1b" />

8. Browse to the VHD directory created earlier in the C:\ directory and click **Next**.:

<img width="710" height="274" alt="11" src="https://github.com/user-attachments/assets/800dcf0e-e983-4ae7-bc63-20e81cdbf9b6" />

8. Click **Finish** at the Summary section

<img width="715" height="535" alt="12" src="https://github.com/user-attachments/assets/37dc353b-c337-4405-832c-42edeb39f77e" />

## Rename the Test Server VM

<img width="1027" height="530" alt="13" src="https://github.com/user-attachments/assets/06ff8314-42d0-4c39-b941-079664ad0f69" />

Note: both of the VM have the same name. By clicking on it you can see the date it was created. The 3rd VM is the one I just imported because the creation date is 3/15/2026.

1. Right-click the imported VM (The 3rd VM) and click **Settings**
2. Click on **Name**
3. Renamed it to **TST-AD-SRV**
4. Click **OK**

<img width="717" height="436" alt="14" src="https://github.com/user-attachments/assets/39e1d117-5161-48cd-83aa-921baadb1464" />














