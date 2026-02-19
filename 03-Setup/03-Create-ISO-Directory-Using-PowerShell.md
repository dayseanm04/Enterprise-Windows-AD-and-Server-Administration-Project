# 03 – Create ISO Directory Using PowerShell  

##  Overview  

In this step, I will dedicated directory is created to store the **Windows Server 2019 ISO installation media**.

For this project, the ISO folder will be created on the **Desktop**.

---

## Objective  

Create a folder named: Win-2019-SRV-ISO

This folder will store the Windows Server 2019 ISO file used during VM deployment.

---

## Tools Used  

- Windows PowerShell on Host Machine  

---

##  Step-by-Step 

###  Step 1 - Open PowerShell  
1. Click **Start**
2. Search for **PowerShell**
3. Right-click **Windows PowerShell**
3. Right-click **Windows PowerShell**

<img width="745" height="387" alt="10" src="https://github.com/user-attachments/assets/15ed600f-2f41-484e-ac51-f3231ac11545" />

Note: I didnt run Powershell as admin because my account is already an Admin Account

###  Step 2 - Navigate to Desktop  

```powershell
cd Desktop
```

To confirm current directory (optional): 

```powershell
dir
```

###  Step 3 - Create the ISO Folder

```powershell
mkdir Win-2019-SRV-ISO
```

<img width="822" height="361" alt="13" src="https://github.com/user-attachments/assets/a1180e61-5ffb-4913-95c7-1042ae348661" />


### Step 4 – Verify the Folder was created

```powershell
dir
```

<img width="990" height="211" alt="1" src="https://github.com/user-attachments/assets/32e688bc-bf89-4ab3-a39b-d2c18e28b5cd" />
<img width="987" height="80" alt="2" src="https://github.com/user-attachments/assets/af4e9545-8957-4419-afe3-970fbf4006de" />


Open File Explorer then Navigate to **Desktop**

<img width="766" height="195" alt="14" src="https://github.com/user-attachments/assets/8433da69-0b68-4c69-8bac-6949a70d702e" />


