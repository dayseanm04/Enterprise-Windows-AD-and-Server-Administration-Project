# 03 – Troubleshoot and Resolve Test Server VM Startup Issue

## Overview

During the setup of the test environment, the **TST-AD-SRV** VM failed to start in Hyper-V. This issue was caused by an **access/permission error related to the ISO file attached to the VM**.

This document outlines the troubleshooting process, root cause, and resolution.

---

##  Problem

When attempting to start the test VM, the following error occurred:
- Virtual machine failed to start
- Access denied error related to ISO file
- Hyper-V could not access the attached installation media

### Error Message:

<img width="506" height="489" alt="VM-error-ss" src="https://github.com/user-attachments/assets/ea4ab7cc-a451-4ca3-822c-9fea07b1dc8e" />

---

##  Root Cause

The issue was caused by:

- The ISO file being located in a directory that **Hyper-V did not have permission to access**

As a result, the VM could not start because it could not access the boot media.

---

##  Resolution

To resolve the issue, I created new ISO folder, copied the ISO file to the new folder and reattached to the **TST-AD-SRV** VM.

---

### Step 1 – Created a New ISO folder in my Desktop

Created a new folder for the test server ISO: **TST-SRV-ISO**

<img width="632" height="276" alt="2" src="https://github.com/user-attachments/assets/5e918337-2fc5-4017-b1f2-2fbb566d14f3" />












