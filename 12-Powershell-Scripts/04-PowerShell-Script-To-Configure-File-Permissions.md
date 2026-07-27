# PowerShell Script To Configure File Permissions

1. Open **notepad** or **text editor**
2. Write the script
3. Save is as **fileperm.ps1**

Note: you can name it whatever you like
- The CSV File is saved in csv-files folder on my Dekstop

```powershell
$SecGroups = Import-Csv "$HOME\Desktop\csv-files\secgroups.csv"
$success = @{
    ForegroundColor = "Green"
    BackgroundColor =  "Black"
}

# Configure permissions for files in company folder

function CompanyFolder {
    foreach($sg in $SecGroups.SecGroup) {    #Loops through every security group
        switch ($sg){
            {$_ -eq "EveryUser-Sec-G"} {    #$_ represent the value of $sg
                Write-Host ""
                Write-Host "Granting $_ Read Permission for the files in the Company-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Company-Folder\policies.txt" /grant "$($_):(R)"
                icacls "$HOME\Desktop\shared-folders\Company-Folder\holiday-schedule.txt" /grant "$($_):(R)"
                break
            }
            {$_ -eq "HR-Sec-G"} {
                Write-Host ""
                Write-Host "Granting $_ Full Access to the files in the Company-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Company-Folder\policies.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\Company-Folder\holiday-schedule.txt" /grant "$($_):(F)"
            }
        }
    }
}

# Configure permissions for files in Customer-Service folder

function CustomerServicesFolder {
    foreach($sg in $SecGroups.SecGroup) {
        switch ($sg){
            {$_ -eq "Customer-Service-Sec-G"} {
                Write-Host " "
                Write-Host "Granting  $_ Full Access to the files in the Customer-Service-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Customer-Services-Folder\faq.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\Customer-Services-Folder\support-temp.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Configure permissions for files in Finance folder

function FinanceFolder {
    foreach($sg in $SecGroups.SecGroup) {
        switch ($sg){
            {$_ -eq "Finance-Sec-G"} {
                Write-Host " "
                Write-Host "Granting  $_ Full Access to the files in the Finance-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\Finance-Folder\payroll.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\Finance-Folder\tax-doc.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Configure permissions for files in HR folder

function HRFolder {
    foreach($sg in $SecGroups.SecGroup) {
        switch ($sg){
            {$_ -eq "HR-Sec-G"} {
                Write-Host " "
                Write-Host "Granting  $_ Full Access to the files in the HR-folder`n" @success
                icacls "$HOME\Desktop\shared-folders\HR-Folder\hiring-doc.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\HR-Folder\onboarding-doc.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Configure permissions for files in IT folder

function ITFolder {
    foreach($sg in $SecGroups.SecGroup) {
        switch ($sg){
            {$_ -eq "IT-Sec-G"} {
                Write-Host " "
                Write-Host "Granting  $_ Full Access of the files in IT-Folder`n" @success
                icacls "$HOME\Desktop\shared-folders\IT-Folder\documentation.txt" /grant "$($_):(F)"
                icacls "$HOME\Desktop\shared-folders\IT-Folder\setup-guides.txt" /grant "$($_):(F)"
                break
            }
        }
    }
}

# Call the Functions

CompanyFolder
CustomerServicesFolder
FinanceFolder
HRFolder
ITFolder
```
