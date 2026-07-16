# 01 - Create Shared Folders

## Overview

In this task creates I will create the shared folders I will use throughout the Windows Server Administration project. I will later on configure  shared folder permissions, NTFS permissions, and access controls for different departments.

### Server: OTCS-DC01

# Shared Folder Structure

| Shared Folder | Purpose | Department Access |
|---------------|---------|-------------------|
| Company-Folder | Company policies, holiday schedule | Everyone |
| HR-Folder | Employee onboarding documents and hiring documents | Human Resources |
| IT-Folder | Setup guides and technical documentation | IT Department |
| Customer-Services-Folder | FAQ documents and customer support templates | Customer Service |
| Finance-Folder | Payroll and tax documents | Finance Department |

### I will use these folders to practice:

- Creating shared folders
- Configuring Share Permissions
- Configuring NTFS Permissions
- Applying security best practices

# Powershell script to create the folders

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **createfolders.ps1**
4. Save it in **Desktop**

```powershell
$foldernames = @("Company-folder", "HR-folder", "IT-folder", "Finance-Folder", "Customer-Services-Folder")

foreach ($foldername in $foldernames) {
	mkdir $foldername
}

Write-Host ""
Write-Host "Folders Created"
```

## Run the script

1. Open **Powershell**
2. cd **Desktop**
3. **./createfolders.ps1**

# Expected Results

<img width="713" height="454" alt="1" src="https://github.com/user-attachments/assets/b7aabcdc-799c-4ce7-8953-245c382e9268" />

<img width="784" height="398" alt="2" src="https://github.com/user-attachments/assets/ca86ea94-f051-4423-b70b-59986f4f9ef0" />

