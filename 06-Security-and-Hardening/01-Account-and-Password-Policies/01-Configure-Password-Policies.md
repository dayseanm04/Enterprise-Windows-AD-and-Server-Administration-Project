# Configure Password Policies

## Overview
Password policy is one of the important security controls on a domain, it decides how strong passwords have to be, how often they expire, and how many old passwords get remembered so users can't just cycle back to an old one. This gets configured through the **Default Domain Policy** in Group Policy Management.

## Open Group Policy Management
1. In **Server Manager**, click **Tools**.

<img width="391" height="208" alt="1" src="https://github.com/user-attachments/assets/781e6a6b-f35f-4830-86ea-6149fa0ea643" />

3. Click **Group Policy Management**.

## View the Default Password Policy
1. Expand **Forest** → **Domain** → `domain.com`.
2. Click on **Default Domain Policy**.

<img width="625" height="364" alt="1" src="https://github.com/user-attachments/assets/319f0c25-b3cf-4e4c-92a7-bd8c395fca30" />

3. Click **OK**.
4. Click the **Settings** tab and scroll down to the **Computer Configuration** section.

<img width="871" height="482" alt="2" src="https://github.com/user-attachments/assets/181e38c4-e5f1-413a-9913-9f7c2cac346e" />

<img width="714" height="528" alt="3" src="https://github.com/user-attachments/assets/8897f496-93ec-4f71-8a41-f0e98e604b87" />

## Configure the Password Policy

1. Right-click **Default Domain Policy** and click **Edit**.

<img width="640" height="298" alt="3 1" src="https://github.com/user-attachments/assets/6e3079c5-1c1a-4468-bd69-19bd0a57e7f4" />

2. Under **Computer Configuration**, go to **Policies** → **Windows Settings** → **Security Settings** → **Account Policies**.

<img width="681" height="341" alt="4" src="https://github.com/user-attachments/assets/7a769c06-32cb-4490-8be5-7c4690e58cf9" />

3. Click **Password Policy**.

<img width="808" height="380" alt="5" src="https://github.com/user-attachments/assets/410becb5-37b6-4833-ae3f-c75521b0c002" />

4. Right-click **Minimum password length**, click **Properties**, set it to **8**, and click **OK**.

<img width="648" height="359" alt="6" src="https://github.com/user-attachments/assets/5980b703-87a1-494d-8db2-e4a92cfda2bd" />

5. Right-click **Minimum password age**, click **Properties**, set it to **60**, and click **OK**.

<img width="639" height="325" alt="7" src="https://github.com/user-attachments/assets/71d0efbe-f31d-4ad4-baed-d8fa4c3948b0" />

## Final Password Policy Settings
| Policy | Value |
|---|---|
| Enforce password history | 24 passwords remembered |
| Maximum password age | 60 days |
| Minimum password age | 1 day |
| Minimum password length | 8 characters |
| Password must meet complexity requirements | Enabled |
| Store passwords using reversible encryption | Disabled |

<img width="833" height="362" alt="8" src="https://github.com/user-attachments/assets/c97f17c6-b5c1-475b-8748-59c2341080e4" />

## Verify
1. Back in Group Policy Management, click **Default Domain Policy**.
2. Click the **Settings** tab and scroll down to the **Computer Configuration** section to confirm the changes took effect.

<img width="950" height="571" alt="9" src="https://github.com/user-attachments/assets/b7fe61c1-fb1d-48da-beb4-87c2c1d029ab" />

3. In PowerShell, ran `gpupdate /force` to push the policy immediately.

<img width="788" height="360" alt="9 1" src="https://github.com/user-attachments/assets/e34346fa-e1d9-40c7-b752-e4792558727e" />

## Click here for the Password policy test [01-Test-Password-Policy-GPO.md](../../08-Testing-and-Validation/06-Group-Policy-and-Security-Tests/01-Test-Password-Policy-GPO.md).

