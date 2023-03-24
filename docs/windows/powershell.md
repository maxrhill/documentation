#powershell command to create organizational unit
New-ADOrganizationalUnit -Name "UserAccounts" -Path "ou=max,DC=max,DC=local"

#powershell command to create a user
New-ADUser -Name "MHill.admin" -DisplayName "MHill.admin" -Path "ou=useraccounts,ou=max,dc=max,dc=local" -UserPrincipalName "MHill.admin@max.local" -Enabled $true -AccountPassword (ConvertTo-SecureString "abc123" -AsPlainText -Force)

#add user account to domain group
Add-ADGroupMember -Identity "domain admins" -Members "mhill.admin"

#set client DNS address (how to find the network on the client)
Set-DnsClientServerAddress -InterfaceIndex 4 -ServerAddresses "192.168.11.200"

#add the client to the domain
Add-Computer -DomainName max.local -Server DC1 -PassThru -Verbose