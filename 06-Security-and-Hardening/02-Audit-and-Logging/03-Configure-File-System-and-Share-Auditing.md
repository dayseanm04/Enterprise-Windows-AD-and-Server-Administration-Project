# Configure File System and Share Auditing

Builds on [**02-Configure-Logon-Logoff-Auditing.md**](./02-Configure-Logon-Logoff-Auditing.md) — same `DC Auditing` GPO, different audit category.

## Overview
The last two GPOs tracked logons and credential checks, but neither tells me anything about what happens to files once someone's logged in. This adds Object Access auditing to the same `DC Auditing` GPO so I can track access to files and shares.

**Heads up:** configuring this policy on isn't enough by itself — it only configures the audit *category*. To actually log activity on a specific folder, you also have to enable auditing on that folder's Security tab (SACL) . That's covered in [11-Configure-File-and-Folder-Auditing.md](./11-Configure-File-and-Folder-Auditing.md).
