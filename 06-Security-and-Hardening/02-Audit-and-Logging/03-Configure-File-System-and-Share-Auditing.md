# Configure File System and Share Auditing

Builds on [**02-Configure-Logon-Logoff-Auditing.md**](./02-Configure-Logon-Logoff-Auditing.md) — same `DC Auditing` GPO, different audit category.

See [**11-Configure-File-and-Folder-Auditing.md**](../../13-Systems-Administration/01-File-Services-and-Access/11-Configure-File-and-Folder-Auditing.md) for pointing this policy at an actual folder.

## Overview
The last two GPOs tracked logons and credential checks, but neither tells me anything about what happens to files once someone's logged in. This adds Object Access auditing to the same `DC Auditing` GPO so I can track access to files and shares.

**Heads up:** configuring this policy on isn't enough by itself — it only configures the audit *category*. To actually log activity on a specific folder, you also have to enable auditing on that folder's Security tab (SACL) . That's covered in [11-Configure-File-and-Folder-Auditing.md](./11-Configure-File-and-Folder-Auditing.md).

**Note:** OTCS-DC01 is also acting as a File Server in this project, thats why I linked this GPO to the Domain Controllers OU

## Open the GPO
1. In Group Policy Management, expand **Forest** → **Domain** → `domain.com` → **Domain Controllers**.

<img width="913" height="403" alt="1" src="https://github.com/user-attachments/assets/4e5b6455-223b-485b-87d4-006b5e83bca3" />

2. Right-click **DC Auditing** and click **Edit**.

<img width="963" height="471" alt="2" src="https://github.com/user-attachments/assets/d6593745-ee99-4c95-a928-8fc20451f603" />

## Navigate to Object Access Audit Policies
Under **Computer Configuration** → **Policies** → **Windows Settings** → **Security Settings** → **Advanced Audit Policy Configuration** → **Audit Policies**, clicked **Object Access**.

<img width="832" height="529" alt="3" src="https://github.com/user-attachments/assets/b22469e8-c0a4-43f0-9430-bd456452ad59" />

## Configure Audit File System
Right-clicked **Audit File System**, clicked **Properties**, checked **Configure the following audit events**, checked both **Success** and **Failure**, and clicked **OK**.

<img width="830" height="420" alt="4" src="https://github.com/user-attachments/assets/7f466de4-705c-4e74-9d37-e7896743634d" />
