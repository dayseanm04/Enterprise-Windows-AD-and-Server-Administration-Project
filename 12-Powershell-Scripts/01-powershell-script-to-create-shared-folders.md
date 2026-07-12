# Powershell script to create folders

```powershell
$foldernames = @("Company-folder", "HR-folder", "IT-folder", "Finance-Folder", "Customer-Services-Folder")

foreach ($foldername in $foldernames) {

	mkdir $foldername

}

Write-Host ""
Write-Host "Folders Created"
```
