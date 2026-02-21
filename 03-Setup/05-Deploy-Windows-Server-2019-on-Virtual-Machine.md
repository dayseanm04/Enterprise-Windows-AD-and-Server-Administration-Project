# 05 – Deploy Windows Server 2019 on Virtual Machine  

## Overview  

In this phase, I will install Windows Server 2019 on the virtual machine I previously created.
This step includes:
- Booting the VM from ISO
- Installing Windows Server 2019 Datacenter (Desktop Experience)
- Configuring the Administrator password

## Objective  

Successfully install and prepare Windows Server 2019 for post-install configuration and Active Directory deployment.

---

## Tools Used  

- Hyper-V Manager  
- Windows Server 2019 ISO  
- Windows Server 2019 Virtual Machine


# Installation Steps  

---

## Step 1 – Start the Virtual Machine  
1. Open **Hyper-V Manager**
2. Double-click the **Windows-2019-SRV** VM
3. Click **Start**

<img width="685" height="561" alt="41" src="https://github.com/user-attachments/assets/6f8acd41-0826-433a-a605-a9f90d380084" />

4. Press any key to boot from the ISO

<img width="759" height="561" alt="42" src="https://github.com/user-attachments/assets/792f621e-b186-4fda-b37d-7048e58872b6" />

If the VM freezes, turn of the VM and 'turn it back on. If that dont work, restart your computer

##  Step 2 – Begin Windows Installation  
1. Select language and region settings
2. Click **Next**

<img width="635" height="470" alt="43" src="https://github.com/user-attachments/assets/6eb42633-91d7-44c7-baf6-f45352819a1e" />

<br/>

3. Click **Install now**

<img width="664" height="480" alt="44" src="https://github.com/user-attachments/assets/103f1f31-bb13-4951-a930-66b343921abe" />

## Step 3 – Select Operating System Edition  

Select: **`Windows Server 2019 Datacenter Evaluation (Desktop Experience)`**
Click **Next**

<img width="652" height="493" alt="45" src="https://github.com/user-attachments/assets/1f29547a-e76c-4c14-a1ad-aa779ea5fbd7" />

##  Step 4 – Accept License Agreement  

1. Accept license terms  
2. Click **Next**

<img width="647" height="484" alt="46" src="https://github.com/user-attachments/assets/ca8a5514-4f2d-490f-b5d9-1325e57d8e71" />

## Step 5 – Choose Installation Type  

Select: **`Custom: Install Windows only (advanced)`**
Click **Next**

<img width="652" height="317" alt="47" src="https://github.com/user-attachments/assets/3d818f81-ce05-4451-ad78-e5159d44ae91" />

## Step 6 – Select Virtual Hard Disk  

1. Choose the **100GB unallocated space**
2. Click **Next**

<img width="652" height="490" alt="48" src="https://github.com/user-attachments/assets/9d01e609-4182-4916-ae7e-e6bb4c4f99d6" />

Note: this is the 100GB I entered when configuring the **`Windows-2019-SRV VM`**

3. Wait for installation to complete

<img width="632" height="304" alt="49" src="https://github.com/user-attachments/assets/fb931272-437a-4552-bba7-7a338e3277cf" />

The VM will restart automatically during installation.

<img width="683" height="514" alt="50" src="https://github.com/user-attachments/assets/9d4161cd-d147-45e0-a83e-8eb48faa4d7e" />

##  Step 7 – Configure Administrator Password  

After installation:

1. Enter Administrator password  
2. Confirm password  
3. Click **Finish**

<img width="756" height="470" alt="51" src="https://github.com/user-attachments/assets/90503522-7b89-46f2-8b9a-86dcbaf41b0b" />

##  Step 8 – Log In  
1. Press **Ctrl + Alt + Delete** (If you have to, I didnt)
2. Enter the Administrator password
3. Log into Windows Server

<img width="581" height="423" alt="52" src="https://github.com/user-attachments/assets/b487558a-5479-4594-b73e-77b8aa12f46c" />

# Post-Installation Network Configuration  

After login, Windows may prompt for network discovery.

Click **Yes** if prompted.

<img width="358" height="411" alt="53" src="https://github.com/user-attachments/assets/deb146f6-0f05-4338-8736-f894c2d4f117" />

#### Windows Server 2019 loads successfully

<img width="780" height="445" alt="55" src="https://github.com/user-attachments/assets/04d0bc44-99b4-42d8-9432-ad9673e3af1a" />











