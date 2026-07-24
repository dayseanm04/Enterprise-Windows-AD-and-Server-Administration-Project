# Powershell script to create folders

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **createfolders.ps1**
4. Save it in **Desktop**

```powershell
mkdir shared-folders
$foldernames = @("Company-Folder", "HR-Folder", "IT-Folder", "Finance-Folder", "Customer-Services-Folder")

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
