# Configure Logon/Logoff Auditing

Builds on [**01-Configure-Account-Logon-Auditing.md**](./01-Configure-Account-Logon-Auditing.md) same **`DC Auditing`** GPO, different audit category.

## Overview
The last GPO tracked credential checks. This one adds logon and logoff events, and account lockouts to the same `DC Auditing` GPO so I can see who logged on, who logged off, and when an account gets locked.

## Open Group Policy Management
1. In Server Manager, click **Tools** → **Group Policy Management**.
2. Expand **Forest** → **Domain**, expand `domain.com`, and click **Domain Controllers**.

<img width="913" height="403" alt="1" src="https://github.com/user-attachments/assets/4e5b6455-223b-485b-87d4-006b5e83bca3" />

3. Right-click **DC Auditing** and click **Edit**.

<img width="963" height="471" alt="2" src="https://github.com/user-attachments/assets/d6593745-ee99-4c95-a928-8fc20451f603" />

## Navigate to Logon/Logoff Audit Policies

Under **Computer Configuration** → **Policies** → **Windows Settings** → **Security Settings** → **Advanced Audit Policy Configuration** → **Audit Policies**, clicked **Logon/Logoff**.

<img width="820" height="352" alt="3" src="https://github.com/user-attachments/assets/56abbc96-8b48-4fb8-9f47-386adadbc5f4" />

## Configure Audit Account Lockout
Right-clicked **Audit Account Lockout**, clicked **Properties**, checked **Configure the following audit events**, checked **Success**, and clicked **OK**.

<img width="809" height="361" alt="4" src="https://github.com/user-attachments/assets/17280ee7-baed-401c-8788-e3198f9a362a" />

**Purpose:** Logs when an account gets locked out for hitting the lockout threshold. This makes it possible to spot a compromised account, a bruteforce attack, or just someone repeatedly typing their password wrong.

**Why Success only, not Failure too?** A lockout event only happens once — the account either locks or it doesn't. There's no "failed lockout" to track, so Success is the only option that applies here.

## Configure Audit Logoff

Right-clicked **Audit Logoff**, clicked **Properties**, checked **Configure the following audit events**, checked **Success**, and clicked **OK**.

<img width="779" height="423" alt="5" src="https://github.com/user-attachments/assets/fb09f627-fffd-4664-b370-7a6dd7768892" />



