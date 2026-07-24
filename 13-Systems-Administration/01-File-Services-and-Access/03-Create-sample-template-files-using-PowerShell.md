# Create Sample Files Using PowerShell

## Overview
As part of setting up the shared folder structure, I needed to populate each folder with sample files. Instead of creating them manually one by one, I wrote a PowerShell script to automate the process. This ensured consistency across all folders and saved time.

## Shared Folders
These are the folders I created in the shared-folders:
- `Company-Folder`
- `Customer-Services-Folder`
- `IT-Folder`
- `HR-Folder`
- `Finance-Folder`

<img width="784" height="398" alt="1" src="https://github.com/user-attachments/assets/ca86ea94-f051-4423-b70b-59986f4f9ef0" />

For each folder, I created two sample files (`sample1.txt` and `sample2.txt`) to act as templates. These sample files can later be used as the basis for creating the actual working files.

## PowerShell Script

```powershell
$sample_files = @("sample1.txt", "sample2.txt")
$folders = @("Company-Folder", "Customer-Services-Folder", "IT-Folder", "HR-Folder", "Finance-Folder")

# Change Directory to shared-folder on Desktop
cd "$HOME\Desktop\shared-folders"

# Loop through the folders
foreach ($f in $folders) {
    cd $f
    foreach ($sf in $sample_files) {
        New-Item -ItemType File $sf -Force
    }
    cd ..
}

Write-Host "Done!"
```

### How it works
- `$sample_files` holds the names of the two template files to create in each folder.
- `$folders` holds the list of shared folder names to loop through.
- The script changes into the `shared-folders` directory on the Desktop.
- For each folder, it enters the folder, creates both sample files using `New-Item -ItemType File`, then returns to the parent directory before moving to the next folder.

## Running the Script
1. Open PowerShell.
2. Change directory to the Desktop:
```powershell
   cd Desktop
```
3. Run the script:
```powershell
   ./createfiles
```

<img width="681" height="394" alt="2" src="https://github.com/user-attachments/assets/c29dc1cf-1548-4a31-b3e1-c8eebd89e95b" />

## Result
Each folder in `shared-folders` now contains `sample1.txt` and `sample2.txt`




