# temppasswordazuread

To assign a common temporary password to all new users, run the following command and replace the TempPW with the password that you would like to provide to your users.

 $PasswordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile

In the next comand, you will set the new temp passorwd for new user in tenant.

 $PasswordProfile.Password = "<<enter-a-secure-password-you-will-remember>>"

That's it guys!!
