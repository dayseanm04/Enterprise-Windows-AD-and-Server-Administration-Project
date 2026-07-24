# PowerShell Script To Create Sample Template Files

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **createfiles.ps1**
4. Save it in **Desktop**

```powershell
$sample_files = @("sample1.txt", "sample2.txt")
$folders = @("Company-Folder", "Customer-Services-Folder", "IT-Folder", "HR-Folder", "Finance-folder")

# Change Directory to shared-folder on Desktop
cd "$HOME\Desktop\shared-folders"

#loop through the folders
foreach ($f in $folders){
	cd $f

	foreach ($sf in $sample_files){
		New-Item -ItemType File $sf -Force
	}
	cd ..
}
Write-Host "Done!"
```
