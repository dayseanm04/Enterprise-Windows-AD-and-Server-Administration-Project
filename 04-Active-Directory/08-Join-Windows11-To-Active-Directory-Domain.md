# Joining a Windows 11 Computer to an Active Directory Domain

## Overview
I will join a Windows 11 host machine to an Active Directory Domain.

## Objective
I will integrate the Windows 11 host computer into the `corp.oaktowncs.com` Active Directory domain to enable centralized administration, domain user authentication, and access to internal network resources.

---

## Environment Overview
* **Client Host:** `comp-a-test` (Windows 11)
* **Target Domain:** `corp.oaktowncs.com`
* **Authorized Account:** `d.moore`

---

## Step-by-Step Guide

### Step 1: Open System Settings

1. Open the **Settings** app on the target machine (`comp-a-test`).
2. Click **System** in the left sidebar.
3. Scroll down and Click **About**.

<img width="625" height="78" alt="1" src="https://github.com/user-attachments/assets/72fc0355-3025-4960-a34e-a4208227bb72" />

---

### Step 2: Access Advanced System Properties
1. Scroll down to the **Related links** section.
2. Click **Domain or workgroup** to open the **System Properties** widow.

<img width="581" height="69" alt="2" src="https://github.com/user-attachments/assets/514fefc4-c5db-4f52-92c5-53687ad7629c" />
<img width="417" height="470" alt="3" src="https://github.com/user-attachments/assets/9043c494-e384-4047-ba4d-b775cec7b421" />

### Step 3: Change workgroup to Domain
1. On the **Computer Name** tab, I will click **Change...**
2. In the **Computer Name/Domain Changes** dialog, select **Domain**.
3. Typed in the domain name: `corp.oaktowncs.com`

<img width="447" height="390" alt="4" src="https://github.com/user-attachments/assets/bd2a0cfa-e129-44d0-b686-9650a58fdf58" />

---

### Step 4: Authenticate and join Domain Join
1. When the **Windows Security** box prompts for credentials, Enter :
2. Click **OK**.

<img width="466" height="405" alt="5" src="https://github.com/user-attachments/assets/cfb724fa-0734-457a-addc-0270553112c0" />

---

### Step 5: Confirm Domain Join and Restart
1. After successful authentication, *"Welcome to the corp.oaktowncs.com domain."* will pop up
2. I will click **OK**.


