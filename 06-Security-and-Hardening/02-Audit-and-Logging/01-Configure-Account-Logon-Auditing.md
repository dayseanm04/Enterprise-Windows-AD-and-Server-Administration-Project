# Configure Account Logon Auditing

## Overview
By default, Windows doesn't log logon attempts on domain controllers, so there's no record if someone's trying to guess passwords. This sets up a GPO to turn on auditing for credential validation, both successful and failed logons get logged so I can actually see what's happening.

## Open Group Policy Management
1. In Server Manager, click **Tools** → **Group Policy Management**.
2. Expand **Forest** → **Domain**, expand `domain.com`, and click **Domain Controllers**.

<img width="913" height="403" alt="1" src="https://github.com/user-attachments/assets/4e5b6455-223b-485b-87d4-006b5e83bca3" />

## Create a GPO for Domain Controller Auditing
1. Right-click the **Domain Controllers** OU and click **Create a GPO in this domain, and Link it here...**

<img width="726" height="364" alt="2" src="https://github.com/user-attachments/assets/fd37c38f-5651-44e2-ba60-c09b7149bd15" />

2. Named it **DC Auditing** — a name that makes its purpose obvious to anyone browsing the GPOs later, rather than something generic.

<img width="698" height="386" alt="3" src="https://github.com/user-attachments/assets/aad57bff-6538-4dc8-bdef-cd9b1fc5ae5a" />

3. Right-clicked **DC Auditing** and clicked **Edit**.
