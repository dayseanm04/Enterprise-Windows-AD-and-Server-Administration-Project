# PowerShell Script To Share Folders

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **grantsmbshareaccess.ps1**

```powershell
$SecGroups = Import-Csv "C:\csv-files\secgroups.csv"

# Output color
$success = @{
    ForegroundColor = "Green"
    BackgroundColor =  "Black"
}

$folders = @("IT-Folder", "Finance-Folder", "Customer-Services-Folder")

Write-Host "After Change: "
foreach ($item in $folders) {
        Get-SmbShareAccess -Name $item
    }

function GrantAccess {
    foreach($sg in $SecGroups.SecGroup) {    #Loops through every security group
        switch ($sg){
            {$_ -eq "IT-Sec-G"} {   #$_ represent the value of $sg
                Write-Host "Granting $($sg) full smb share to the access IT-Folder`n" @success
                Grant-SmbShareAccess -Name "IT-Folder" -AccountName $sg -AccessRight Full -Force
                Revoke-SmbShareAccess -Name $folders[0] -AccountName "Everyone" -Force
            }
            {$_ -eq "Finance-Sec-G"} {
                Write-Host "Granting $($sg) full smb share access to the access Finance-Folder`n" @success
                Grant-SmbShareAccess -Name "Finance-Folder" -AccountName $sg -AccessRight Full -Force
                Revoke-SmbShareAccess -Name $folders[1] -AccountName "Everyone" -Force
            }
            {$_ -eq "Customer-Service-Sec-G"} {
                Write-Host "Granting $($sg) full smb share access to the Customer-Service-Folder`n" @success
                Grant-SmbShareAccess -Name "Customer-Services-Folder" -AccountName $sg -AccessRight Full -Force
                Revoke-SmbShareAccess -Name $folders[2] -AccountName "Everyone" -Force
            }
        }
    }
}

GrantAccess
```
