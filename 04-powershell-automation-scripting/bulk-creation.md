# Bulk creation

in powershell </br>

``` powershell {
    New-ADUser `
-Name "Jae Jeon" `
-GivenName "Jae" `
-Surname "Jeon" `
-SamAccountName "jjeon" `
-UserPrincipalName "jjeon@company.local" `
-Path "OU=Mangement,DC=comapny,DC=local" `
-AccountPassword (ConvertTo-SecureString "Welcome1@" -AsPlainText -Force) `
-Enabled $true


