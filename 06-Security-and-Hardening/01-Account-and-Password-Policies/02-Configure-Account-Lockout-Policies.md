# Configure Account Lockout Policies

Related: [**01-Configure-Password-Policies.md**](./01-Configure-Password-Policies.md)

## Overview
Account lockout policy protects against brute-force attacks, if someone (or something automated) keeps guessing a user's password, the account locks after a set number of failed attempts instead of letting them keep trying indefinitely. Like password policy, this is configured through the **Default Domain Policy** in Group Policy Management.

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

## Configure the Account Lockout Policy

1. Right-click **Default Domain Policy** and click **Edit**.
2. Under **Computer Configuration**, go to **Policies** → **Windows Settings** → **Security Settings** → **Account Policies**.
