# PowerShell Script To Create Sample Template Files

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **createfiles.ps1**
4. Save it in **Desktop**

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
