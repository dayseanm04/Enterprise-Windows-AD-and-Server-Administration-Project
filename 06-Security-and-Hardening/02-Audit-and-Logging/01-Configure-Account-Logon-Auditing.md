# Configure Account Logon Auditing

## Overview
By default, Windows doesn't log logon attempts on domain controllers, so there's no record if someone's trying to guess passwords. This sets up a GPO to turn on auditing for credential validation, both successful and failed logons get logged so I can actually see what's happening.

## Open Group Policy Management
1. In Server Manager, click **Tools** → **Group Policy Management**.
2. Expand **Forest** → **Domain**, expand `domain.com`, and click **Domain Controllers**.
