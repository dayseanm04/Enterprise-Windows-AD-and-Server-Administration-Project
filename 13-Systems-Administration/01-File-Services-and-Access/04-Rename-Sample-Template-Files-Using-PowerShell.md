# Rename Sample Files Using PowerShell

## Overview
With the sample files (`sample1.txt` and `sample2.txt`) already created in each shared folder, the next step was to rename them. I wrote a PowerShell script using a `switch` statement to rename the files differently depending on which folder they were in.

## Shared Folders
The following folders exist under `shared-folders`:

- `Company-Folder`
- `Customer-Services-Folder`
- `IT-Folder`
- `HR-Folder`
- `Finance-Folder`

<img width="784" height="398" alt="1" src="https://github.com/user-attachments/assets/ca86ea94-f051-4423-b70b-59986f4f9ef0" />

## File Naming Reference
Each folder's sample files were renamed to match its purpose:

| Folder | sample1.txt | sample2.txt |
|---|---|---|
| Company-Folder | policies.txt | holiday-schedule.txt |
| HR-Folder | onboarding-doc.txt | hiring-doc.txt |
| Customer-Services-Folder | faq.txt | support-temp.txt |
| IT-Folder | setup-guides.txt | documentation.txt |
| Finance-Folder | payroll.txt | tax-doc.txt |

## Powershell script

```powershell
$folders = @(
    "Company-Folder",
    "Customer-Services-Folder",
    "IT-Folder",
    "HR-Folder",
    "Finance-Folder"
)

Set-Location "$HOME\Desktop\shared-folders"

foreach ($folder in $folders) {

    Set-Location $folder

    switch ($folder) {

        "Company-Folder" {
            Write-Host "[$folder] Renaming sample1.txt -> policies.txt"
            Rename-Item "sample1.txt" "policies.txt"

            Write-Host "[$folder] Renaming sample2.txt -> holiday-schedule.txt"
            Rename-Item "sample2.txt" "holiday-schedule.txt"
        }

        "HR-Folder" {
            Write-Host "[$folder] Renaming sample1.txt -> onboarding-doc.txt"
            Rename-Item "sample1.txt" "onboarding-doc.txt"

            Write-Host "[$folder] Renaming sample2.txt -> hiring-doc.txt"
            Rename-Item "sample2.txt" "hiring-doc.txt"
        }

        "Customer-Services-Folder" {
            Write-Host "[$folder] Renaming sample1.txt -> faq.txt"
            Rename-Item "sample1.txt" "faq.txt"

            Write-Host "[$folder] Renaming sample2.txt -> support-temp.txt"
            Rename-Item "sample2.txt" "support-temp.txt"
        }

        "IT-Folder" {
            Write-Host "[$folder] Renaming sample1.txt -> setup-guides.txt"
            Rename-Item "sample1.txt" "setup-guides.txt"
            
            Write-Host "[$folder] Renaming sample2.txt -> documentation.txt"
            Rename-Item "sample2.txt" "documentation.txt"
        }

        "Finance-Folder" {
            Write-Host "[$folder] Renaming sample1.txt -> payroll.txt"
            Rename-Item "sample1.txt" "payroll.txt"
            
            Write-Host "[$folder] Renaming sample2.txt -> tax-doc.txt"
            Rename-Item "sample2.txt" "tax-doc.txt"
        }
    }

    Set-Location ..
}

Write-Host "Done!"
```

### How it works
- `$folders` holds the list of folder names to loop through.
- The script sets its location to the `shared-folders` directory on the Desktop.
- For each folder, it moves into that folder, then uses a `switch` statement to match the folder name and rename that folder's `sample1.txt` and `sample2.txt` to the appropriate file names.
- After each folder is processed, the script moves back up one directory (`Set-Location ..`) before continuing to the next.

## Running the Script
1. Open Notepad or VS Code and save the script as `renamefiles.ps1`.
2. Open PowerShell.
3. Change directory to the Desktop:
```powershell
   cd Desktop
```
4. Run the script:
```powershell
   ./renamefiles.ps1
```
The script ran successfully:





