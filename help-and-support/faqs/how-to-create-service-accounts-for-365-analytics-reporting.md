# How to create service accounts for 365 Analytics reporting

365 Analytics Reporting uses a service account to collect data from O365 tenants. Service accounts are used to collect data via PowerShell in cases where data can’t be collected via GraphAPI. You can create service accounts using PowerShell and Microsoft 365 Admin Center.

Your organization will not be charged by Microsoft for this account as it does not require an Office 365 license.

### Creating a Service Account using PowerShell

We recommend that you use PowerShell to create service accounts because this method contains fewer steps.&#x20;

{% hint style="info" %}
Before creating an account, make sure that you're connected to Office 365. If you are not, then follow these steps to connect to Office 365:

1. Install the Microsoft Online Service Module on your system.
2. Open Windows PowerShell and copy and paste the following commands:

```powershell
    $Office365credentials = Get-Credential
    Import-Module MSOnline
    Connect-MsolService -Credential $Office365credentials
```

3. When prompted, enter the username and password of the Office 365 Administrator account. Your account will be connected to Office 365 in PowerShell.
{% endhint %}

Follow these steps to create a service account:

After your account is connected to Office 365 in PowerShell, follow these steps to create a service account:

1. Modify the following line and set `company.onmicrosoft.com` to match your own Office 365 `.onmicrosoft.com` domain.

```
New-MSolUser -DisplayName "Service Account for 365 Analytics" -UserPrincipalName "365Analytics@company.onmicrosoft.com" -Password "Password123" -PasswordNeverExpires $true -ForceChangePassword $false
```

2. Replace the password with a secure password. We recommend a password of 10 characters or more and including capital and lowercase letters, numbers, and special characters.
3. Add the new account to the ‘Global reader’. You can do this by copying and pasting the following line into the PowerShell window.

```
Add-MSOLRoleMember –RoleName "Global reader" –RoleMemberEmailAddress 365Analytics@company.onmicrosoft.com
```

4. Check if the service account was set correctly by running the following PowerShell commands:

```powershell
$role = Get-MsolRole -RoleName "Global reader"
Get-MsolRoleMember -RoleObjectId $role.ObjectId
```

{% hint style="info" %}
You'll not receive a confirmation if the commands are successful.
{% endhint %}

### Creating a Service Account using the Microsoft 365 Admin Center

You can create a service account via the Microsoft 365 Admin Center, however, you'll still need to run a final PowerShell cmdlet to ensure that the password doesn't expire.

**To create a Service Account using the Microsoft 365 Admin Center**

1. On the Admin home page, go to **Users** > **Active users** and select **Add a user**.
2. Enter the display name as Service Account for 365 Analytics and the user name as 365Analytics.
3. Ensure that the domain is the `company.onmicrosoft.com`.
4. Select **Let me create a password** and enter the new password.
5. Ensure that the **Require this user to change their password when they first sign-in** option is not selected.
6. In the Product Licenses page, choose **Create user without product license**.
7. In the Optional settings page, choose **Admin Center** access and select **Global Reader**.
8. Review the data and select **Finish adding** on the last page.

{% hint style="info" %}
If the password of the service account has expired or needs to be changed, you must change it in Office and in the Tenant Management System Client.
{% endhint %}

If your company policy allows passwords to never expire, you can do so using the following PowerShell command:

{% code fullWidth="false" %}
```powershell
Set-MsolUser -UserPrincipalName 365Analyitcs@company.onmicrosoft.com -PasswordNeverExpires $true
```
{% endcode %}

### Connecting your tenant

365 Analytics requires a Microsoft Application consent. 365 Analytics Reporting uses application consent to collect data from your Office 365 tenant. Application consent is used to collect data via Graph API.

For information on how to authorize the 365 Analytics Application for read-only access to your Office 365 tenant, see [How to connect your 365 tenant for data collection](how-do-i-connect-the-microsoft-tenant-for-data-collection.md).
