# Configure File System and Share Auditing

Builds on [**02-Configure-Logon-Logoff-Auditing.md**](./02-Configure-Logon-Logoff-Auditing.md) — same `DC Auditing` GPO, different audit category.

## Overview
The last two GPOs tracked logons and credential checks, but neither tells me anything about what happens to files once someone's logged in. This adds Object Access auditing to the same `DC Auditing` GPO so I can track access to files and shares.
