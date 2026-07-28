# Test Company-Folder Access

## Overview
Now that the folders are shared and permissions are set, I want to actually test that the permissions work the way they're supposed to. For this test, I logged in as `d.moore` (Daniel Moore, a test user in the IT department — not a real person, just part of my project). `d.moore` is a member of the `EveryUser-Sec-G` group, which should only have Read permission on the files inside the Company-Folder, and Read & Execute on the Company-Folder itself. This test confirms that the permissions actually working.

## Verify the Logged-In User
Opened PowerShell to confirm I'm logged in as `d.moore`:

<img width="585" height="279" alt="1" src="https://github.com/user-attachments/assets/524c800f-daaf-464e-85a1-5f471dc860f9" />

## Accessing the Share via the GUI

### 1. Open File Explorer and Click Network

<img width="621" height="412" alt="1" src="https://github.com/user-attachments/assets/fb48876b-1ab9-431c-9008-ed2a0eeb4a98" />

### 2. Click OTCS-DC01

<img width="639" height="415" alt="2" src="https://github.com/user-attachments/assets/7d88777a-2051-41ad-b985-4e42cbc5ac8f" />

### 3. Click Company-Folder
Able to see the contents of the Company-Folder:

<img width="808" height="408" alt="3" src="https://github.com/user-attachments/assets/854b7e42-83b7-4056-8de1-3079551dcfcb" />

### 4. Open a File
Opened the `holiday-schedule` file with no issues:

