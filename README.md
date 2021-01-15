# Update-GAL
Update recipient in bulk in Office 365 after implementing GAL segmentation
#############################################

$mbs =Get-Mailbox -ResultSize unlimited

foreach ($mb in $mbs){

    Update-Recipient -Identity $mb.UserPrincipalName

    Write-Host "Updating done...." $mb.DisplayName -ForegroundColor Green
}
