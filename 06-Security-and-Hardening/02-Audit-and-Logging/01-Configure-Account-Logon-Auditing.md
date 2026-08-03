# Configure Account Logon Auditing

## Overview
By default, Windows doesn't log logon attempts on domain controllers, so there's no record if someone's trying to guess passwords. This sets up a GPO to turn on auditing for credential validation, both successful and failed logons get logged so I can actually see what's happening.

## Open Group Policy Management
1. In Server Manager, click **Tools** → **Group Policy Management**.
2. Expand **Forest** → **Domain**, expand `domain.com`, and click **Domain Controllers**.

<img width="913" height="403" alt="50" src="https://github.com/user-attachments/assets/4e5b6455-223b-485b-87d4-006b5e83bca3" />

## Create a GPO for Domain Controller Auditing
1. Right-click the **Domain Controllers** OU and click **Create a GPO in this domain, and Link it here...**
