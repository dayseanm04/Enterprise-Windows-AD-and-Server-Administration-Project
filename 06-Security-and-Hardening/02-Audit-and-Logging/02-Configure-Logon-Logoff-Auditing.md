# Configure Logon/Logoff Auditing

Builds on [**01-Configure-Account-Logon-Auditing.md**](./01-Configure-Account-Logon-Auditing.md) same **`DC Auditing`** GPO, different audit category.

## Overview
The last GPO tracked credential checks. This one adds logon and logoff events, and account lockouts to the same `DC Auditing` GPO so I can see who logged on, who logged off, and when an account gets locked.

## Open Group Policy Management
1. In Server Manager, click **Tools** → **Group Policy Management**.
2. Expand **Forest** → **Domain**, expand `domain.com`, and click **Domain Controllers**.

<img width="913" height="403" alt="1" src="https://github.com/user-attachments/assets/4e5b6455-223b-485b-87d4-006b5e83bca3" />

3. Right-click **DC Auditing** and click **Edit**.

<img width="963" height="471" alt="4" src="https://github.com/user-attachments/assets/d6593745-ee99-4c95-a928-8fc20451f603" />

## Navigate to Logon/Logoff Audit Policies

Under **Computer Configuration** → **Policies** → **Windows Settings** → **Security Settings** → **Advanced Audit Policy Configuration** → **Audit Policies**, clicked **Logon/Logoff**.

