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

**Why audit this?** Logs when files or folders are accessed on the local disk — who read, changed, or deleted something, and whether they were allowed to. Auditing both Success and Failure means I can see legitimate access and blocked/denied attempts, which matters for spotting someone poking around files they shouldn't have access to.

## Configure Audit File Share

Right-clicked **Audit File Share**, clicked **Properties**, checked **Configure the following audit events**, checked both **Success** and **Failure**, and clicked **OK**.

<img width="848" height="391" alt="5" src="https://github.com/user-attachments/assets/7a1f1c98-5f32-42cf-a481-78d82ed19c4b" />

**Why audit this separately from File System?** Audit File System covers the local folder/file access, but File Share auditing specifically tracks access to files over an SMB share — like the shared folders I set up earlier in this project (Company-Folder, HR-Folder, etc.). Since those folders are accessed almost entirely over the network rather than locally, this is the setting that actually matters for tracking who's accessing them.

<img width="860" height="481" alt="6" src="https://github.com/user-attachments/assets/d7193e0c-d389-42d8-97cb-f2886bea5253" />

## Configured Object Access Policies
| Policy | Setting |
|---|---|
| Audit File Share | Success and Failure |
| Audit File System | Success and Failure |


