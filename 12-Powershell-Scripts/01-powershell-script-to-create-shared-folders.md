# Powershell script to create folders

1. open notepad
2. write the script
3. save is as createfolders.ps1
4. save it in desktop

```powershell
$foldernames = @("Company-folder", "HR-folder", "IT-folder", "Finance-Folder", "Customer-Services-Folder")

foreach ($foldername in $foldernames) {
	mkdir $foldername
}

Write-Host ""
Write-Host "Folders Created"
```

## Run the scrip

1. Open powershell
2. cd Desktop
3. ./createfolders.ps1
