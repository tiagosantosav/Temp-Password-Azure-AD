# Set a temporary password to news users in Azure AD

To assign a common temporary password to all new users, you can just run the following command and replace the TempPW with the password that you would like to provide to your users.

 $PasswordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile

In the following command, you will set the new temp password for a new user in the tenant.

 $PasswordProfile.Password = "xxxxxxxxxxx"

Finally, you can create a new user with this command.

 New-AzureADUser -DisplayName "New User" -PasswordProfile $PasswordProfile -UserPrincipalName "NewUser@labtenantname.com" -AccountEnabled $true -MailNickName "Newuser"

That's it guys!!
