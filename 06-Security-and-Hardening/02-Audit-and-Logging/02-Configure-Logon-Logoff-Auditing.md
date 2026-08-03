# Configure Logon/Logoff Auditing

Builds on [**01-Configure-Account-Logon-Auditing.md**](./01-Configure-Account-Logon-Auditing.md) same **`DC Auditing`** GPO, different audit category.

## Overview
The last GPO tracked credential checks. This one adds logon and logoff events, and account lockouts to the same `DC Auditing` GPO so I can see who logged on, who logged off, and when an account gets locked.

## Open Group Policy Management
1. In Server Manager, click **Tools** → **Group Policy Management**.
2. Expand **Forest** → **Domain**, expand `domain.com`, and click **Domain Controllers**.

