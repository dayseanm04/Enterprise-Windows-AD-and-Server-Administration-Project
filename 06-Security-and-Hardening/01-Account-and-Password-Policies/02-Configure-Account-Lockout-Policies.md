# Configure Account Lockout Policies

Related: [**01-Configure-Password-Policies.md**](./01-Configure-Password-Policies.md)

## Overview
Account lockout policy protects against brute-force attacks, if someone (or something automated) keeps guessing a user's password, the account locks after a set number of failed attempts instead of letting them keep trying indefinitely. Like password policy, this is configured through the **Default Domain Policy** in Group Policy Management.

## Open Group Policy Management
1. In **Server Manager**, click **Tools**.

<img width="391" height="208" alt="1" src="https://github.com/user-attachments/assets/781e6a6b-f35f-4830-86ea-6149fa0ea643" />

3. Click **Group Policy Management**.
4. Expand **Forest** → **Domain** → `domain.com`.
5. Click on **Default Domain Policy**.

<img width="625" height="364" alt="2" src="https://github.com/user-attachments/assets/319f0c25-b3cf-4e4c-92a7-bd8c395fca30" />

6. Click **OK**.

## Configure the Account Lockout Policy

1. Right-click **Default Domain Policy** and click **Edit**.

<img width="640" height="298" alt="3" src="https://github.com/user-attachments/assets/6e3079c5-1c1a-4468-bd69-19bd0a57e7f4" />

2. Under **Computer Configuration**, go to **Policies** → **Windows Settings** → **Security Settings** → **Account Policies**.

<img width="681" height="341" alt="4" src="https://github.com/user-attachments/assets/7a769c06-32cb-4490-8be5-7c4690e58cf9" />

3. Click **Account Lockout Policy**.

<img width="829" height="379" alt="5" src="https://github.com/user-attachments/assets/92f63dc9-b1ef-48a5-85ec-a60931e0b029" />

### Configure Lockout Duration

Right-clicked **Account lockout duration**, clicked **Properties**, checked **Define this policy setting**, and set it to **60** minutes.

<img width="759" height="394" alt="6" src="https://github.com/user-attachments/assets/a1656c11-66d2-4770-ab6b-fd784e56cb52" />

Clicked **OK**, **OK**.

<img width="757" height="531" alt="7" src="https://github.com/user-attachments/assets/50e7fb81-ebbe-410a-be71-c0afd50d1fc3" />

**Note:** the **Account lockout threshold** was automatically set to **5 invalid logon attempts** as soon as I defined set the lockout duration to 60.

### Configure Reset Account Lockout Counter After

Right-clicked **Reset account lockout counter after**, clicked **Properties**, and set it to **30** minutes.

<img width="775" height="367" alt="8" src="https://github.com/user-attachments/assets/5ada06cc-9ab6-431c-b475-5c2ca9cd26ea" />

### Configure Allow Administrator Account Lockout
Right-clicked **Allow Administrator account lockout**, clicked **Properties**, and checked **Define this policy setting**.

<img width="747" height="342" alt="9" src="https://github.com/user-attachments/assets/67f6d6a4-8b75-4f48-a6ac-90cf9e6f988d" />

## Final Account Lockout Policy Settings
| Policy | Value |
|---|---|
| Account lockout duration | 60 minutes |
| Account lockout threshold | 5 invalid logon attempts |
| Reset account lockout counter after | 30 minutes |
| Allow Administrator account lockout | Enabled |

<img width="883" height="387" alt="10" src="https://github.com/user-attachments/assets/6d1f8ddb-fc45-4e00-b4a9-a000ed12fd40" />

## Verify
1. Back in Group Policy Management, click **Default Domain Policy**.
2. Click the **Settings** tab and scroll down to the **Computer Configuration** section to confirm the changes took effect.

<img width="930" height="548" alt="11" src="https://github.com/user-attachments/assets/e1e42e32-7c54-493a-9c1d-288fd961111b" />

3. In PowerShell, ran `gpupdate /force` to push the policy immediately.

<img width="788" height="360" alt="12" src="https://github.com/user-attachments/assets/e34346fa-e1d9-40c7-b752-e4792558727e" />

## Click here for the Password policy test** [01-Test-Password-Policy-GPO.md](../../08-Testing-and-Validation/06-Group-Policy-and-Security-Tests/02-Test-Account-Lockout-GPO.md).
