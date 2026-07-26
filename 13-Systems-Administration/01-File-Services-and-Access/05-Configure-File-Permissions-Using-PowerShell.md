# Configure File Permissions Using PowerShell

## Overview

Configure NTFS file permissions so each security group only has the access to the files they need. Rather than setting permissions manually through the GUI, I wrote a PowerShell script using `icacls` to grant permissions based on data imported from a CSV file.

