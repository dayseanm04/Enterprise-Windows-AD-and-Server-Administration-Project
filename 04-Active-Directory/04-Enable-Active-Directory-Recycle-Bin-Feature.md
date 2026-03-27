# 04 - Enable Active Directory Recycle Bin Feature

## Overview
In this task I will enable the Active Directory Recycle Bin feature using the **Active Directory Administrative Center (ADAC)**. This feature allows administrators to restore deleted objects such as users, groups, and OUs.

---

## Objectives
- Enable the Active Directory Recycle Bin feature
- Verify that the Recycle Bin is active

---

## Steps to Enable AD Recycle Bin

### 1. Open Active Directory Administrative Center
- Open **Server Manager**
- Click **Tools**
- Select **Active Directory Administrative Center**

---

### 2. Navigate to the Domain
- In ADAC, click on `corp (local)`

<img width="986" height="538" alt="1" src="https://github.com/user-attachments/assets/c9a395a6-5a86-4aee-ab7f-850e027aee73" />

---

### 3. Enable Recycle Bin
- In the right-hand **Tasks** pane
- Click **Enable Recycle Bin**

<img width="691" height="420" alt="2" src="https://github.com/user-attachments/assets/f0b01689-4952-472b-8b8c-1a213293d7a5" />

- Click **OK** to confirm

### 4. Confirm the Action
- A confirmation window will appear
- Click **OK**

<img width="399" height="200" alt="3" src="https://github.com/user-attachments/assets/de9d3f14-d9f5-4547-b174-e50322d9b6bf" />

---

### 5. Refresh ADAC
- Click the **Refresh** button (top-right)

<img width="993" height="546" alt="4" src="https://github.com/user-attachments/assets/a1289b20-7b8f-4c11-8093-5171fb129bf3" />

---

## Verification

<img width="937" height="446" alt="5" src="https://github.com/user-attachments/assets/b7bd159a-37c0-4493-9a2e-add2d313145d" />

After enabling the feature:
- A **Deleted Objects** container will appear in the domain
- This confirms that the Recycle Bin is active
- Deleted objects can now be restored
