# Test Company-Folder Access

## Overview
Now that the folders are shared and permissions are set, I want to actually test that the permissions work the way they're supposed to. For this test, I logged in as `d.moore` (Daniel Moore, a test user in the IT department — not a real person, just part of my project). `d.moore` is a member of the `EveryUser-Sec-G` group, which should only have Read permission on the files inside the Company-Folder, and Read & Execute on the Company-Folder itself. This test confirms that the permissions actually working.

## Verify the Logged-In User
Opened PowerShell to confirm I'm logged in as `d.moore`:

<img width="585" height="279" alt="1" src="https://github.com/user-attachments/assets/524c800f-daaf-464e-85a1-5f471dc860f9" />

## Accessing the Share via the GUI

### 1. Open File Explorer and Click Network
