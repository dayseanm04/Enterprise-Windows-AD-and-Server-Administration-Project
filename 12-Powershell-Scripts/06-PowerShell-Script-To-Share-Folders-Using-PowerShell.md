# PowerShell Script To Share Folder Folder

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **sharefolder.ps1**

 
```powershell
$SecGroups = Import-Csv "C:\csv-files\secgroups.csv"

# Output color
$success = @{
    ForegroundColor = "Green"
    BackgroundColor =  "Black"
}

function ShareFolder {
    foreach($sg in $SecGroups.SecGroup) {    #Loops through every security group
        switch ($sg){
            {$_ -eq "HR-Sec-G"} {   #$_ represent the value of $sg
                Write-Host ""
                Write-Host "Sharing HR-Folder`n" @success
                New-SmbShare `
                    -Name "HR-Folder" `
                    -Path "C:\shared-folders\HR-Folder"
            }
            {$_ -eq "IT-Sec-G"} {
                Write-Host ""
                Write-Host "Sharing IT-Folder`n" @success
                New-SmbShare `
                    -Name "IT-Folder" `
                    -Path "C:\shared-folders\IT-Folder"
            }
            {$_ -eq "Finance-Sec-G"} {
                Write-Host ""
                Write-Host "Sharing Finance-Folder`n" @success
                New-SmbShare `
                    -Name "Finance-Folder" `
                    -Path "C:\shared-folders\Finance-Folder"
            }
            {$_ -eq "Customer-Service-Sec-G"} {
                Write-Host ""
                Write-Host "Sharing Customer-Services-Folder`n" @success
                New-SmbShare `
                    -Name "Customer-Services-Folder" `
                    -Path "C:\shared-folders\Customer-Services-Folder"
            }
        }
    }
}

ShareFolder
```
