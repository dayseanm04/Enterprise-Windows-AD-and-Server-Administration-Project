# PowerShell Script To Configure Folder Permissions

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **folderperm.ps1**

# PowerShell Script To Configure Folder Permissions

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **folderperm.ps1**

**Note**
- I moved the **CSV File** and the **shared-folders** is saved in csv-files folder the C:\ drive

```powershell
$SecGroups = Import-Csv "C:\csv-files\secgroups.csv"

# Output color
$success = @{
    ForegroundColor = "Green"
    BackgroundColor =  "Black"
}

# Configure permissions for the shared folders

function ShrdFolderPerm {
    foreach($sg in $SecGroups.SecGroup) {    #Loops through every security group
        switch ($sg){
            {$_ -eq "EveryUser-Sec-G"} {    #$_ represent the value of $sg
                Write-Host ""
                Write-Host "Granting $_ Read Permision to the Company-Folder`n" @success
                icacls "C:\shared-folders\Company-Folder\" /grant "$($_):(RX)"
            }
            {$_ -eq "HR-Sec-G"} {
                Write-Host ""
                Write-Host "Granting $_ Full Access to the HR-Folder and Company-Folder`n" @success
                icacls "C:\shared-folders\HR-Folder" /grant "$($_):(F)"
                icacls "C:\shared-folders\Company-Folder" /grant "$($_):(F)"
            }
            {$_ -eq "IT-Sec-G"} {
                Write-Host ""
                Write-Host "Granting $_ Full Access to the IT-Folder`n" @success
                icacls "C:\shared-folders\IT-Folder" /grant "$($_):(F)"
            }
            {$_ -eq "Finance-Sec-G"} {
                Write-Host ""
                Write-Host "Granting $_ Full Access to the Finance-Folder`n" @success
                icacls "C:\shared-folders\Finance-Folder" /grant "$($_):(F)"
            }
            {$_ -eq "Customer-Service-Sec-G"} {
                Write-Host ""
                Write-Host "Granting $_ Full Access to the Customer-Service-Folder`n" @success
                icacls "C:\shared-folders\Customer-Services-Folder" /grant "$($_):(F)"
            }
        }
    }
}

ShrdFolderPerm
```
