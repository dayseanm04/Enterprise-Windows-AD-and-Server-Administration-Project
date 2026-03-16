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

<img width="628" height="289" alt="3" src="https://github.com/user-attachments/assets/b7b14780-7457-4081-a973-7a18f127cb99" />

2. Click on **Export..**
3. Browse to the export folder (**SRV2019_Export**) created earlier:

<img width="601" height="196" alt="4" src="https://github.com/user-attachments/assets/31bf5e61-547f-43fc-8ac5-25857993cd06" />

4. Click **Export**

<img width="695" height="300" alt="5" src="https://github.com/user-attachments/assets/baebde5a-e2fb-40a1-afc5-3b9b1e307772" />

Export completed

### Step 4 – Import the Virtual Machine

After the export completes, import the virtual machine.

In Hyper-V Manager 

1. Click **Import Virtual Machine**

<img width="741" height="286" alt="6" src="https://github.com/user-attachments/assets/e0db6320-e78d-4c8f-b4f7-4ed908e11b83" />












