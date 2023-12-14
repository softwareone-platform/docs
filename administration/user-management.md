---
description: >-
  Administrators can add new users and manage existing users and their
  permissions through the User Management module.
---

# User Management

***

The User Management module can be accessed by navigating to **Set up** > **User Management**.&#x20;

On the User Management page, administrators can add new users, manage existing users (edit, delete, and restore), and control access to features and associated functionalities.&#x20;

Watch the following video tutorial on how to use User Management:

{% embed url="https://vimeo.com/889153436" %}

## Adding new users

Only administrators can create new user accounts in the Client Portal.&#x20;

**To add a user account**

1. Navigate to **Set up > User management** and select **Add User**. The **Add New User** page opens.
2. Under **User Details**, provide a valid email address and the first and last name of the user. Note that if the email address already exists in the Client Portal and it belongs to a deleted user, you can [restore the user](user-management.md#special-case-restore-users-from-add-users).
3. Confirm that the user details are correct.&#x20;
4. Select **No, Thanks** to add the user manually.
5. Under **Account Security**, move the slider to enable or disable security settings as needed:
   * **Multi-Factor-Authentication (MFA) after inactivity**: Select to prompt users for MFA if they are inactive for a certain period. You can configure the number of days after which users must re-authenticate.
   * **Multi-Factor-Authentication (MFA) for every login**: Select to prompt users for MFA each time they sign in to the account.
   * **Automated account blocking**: Select to block the account if the user is inactive for a certain period.&#x20;
   * **Password expiration**: Select to prompt users to change their password after a certain number of days.
6. Under **Feature Permissions**, choose whether you want to create an admin user or a basic user, and then assign permissions. Selecting **Show All Permissions** displays all features and associated functionalities, allowing you to enable or disable permissions as needed.
7. Under **Company Access**, choose the companies that the user will procure for. You can select all companies or a specific company.
8. Under **Procurement Settings**, specify procurement settings for the new user. Note that the procurement settings are specific to SoftwareOne entities. If users can purchase from several SoftwareOne entities (for example, SoftwareOne Finland, SoftwareOne Canada, and SoftwareOne Australia), all entities can have different settings.
9. Under **Catalog and Documents**, choose if you want the user to view catalogs and documents (like quotes, orders, and invoices) from specific SoftwareOne entities only. You can choose the legal entities after enabling the setting.
10. Under **Spend Management Access**, specify the user's level of access to Spend Management.
    * **Full Access**: Grants access to all data without any restrictions. By default, each user has full access.
    * **Accounts**: Grants access to specific providers, cloud accounts, and subscriptions. Choose the option and then select **Next** to define the access. Note that defining access at the provider level grants access to all accounts and subscriptions, including those added in the future. Users will get access to new entities automatically. The same rule applies to defining access at the account (tenant) level.
    * **Custom Groups**: Grants access to certain custom groups only. Choose the option and then select **Next** to choose custom groups. Note that selecting a group allows users to see all resources assigned to that group, and all cloud spend data related to those resources.
11. Under **Collaboration Site Access**, specify the level of access for each folder within the Collaboration Site:
    * **None**: Access is not permitted. Users cannot view the workspace and it's not displayed in the list of available workspaces.
    * **Read**: Users can access all elements of the workspace in read-only mode. Users can browse through a directory structure, list files, and download them. Modification of resources is not allowed.
    * **Read, Write**: Users have all permissions included in the Read mode. Additionally, users can upload files, create directories and links, delete files, directories, and links.
12. Review the summary and select **Next** to continue.
13. Choose recipients for the welcome email and select **Complete**. Note that the welcome email can only be sent once. If users delete or lose their welcome email, they can [reset their password](../using-the-client-portal/password-reset.md) from the sign-in page.&#x20;

{% hint style="info" %}
**NOTES**

* The **Procurement Settings** section is displayed only if you've selected at least one Procurement permission under Feature Permissions.
* The **Catalog and Documents** section is displayed only if you've enabled Company Access for the user.
* The **Collaboration Site Access** section is displayed only if you've enabled the Collaboration Site permission under Feature Permissions.
{% endhint %}

***

## Copying permissions from one user to another <a href="#how-to-copy-user-permissions-from-a-source-to-target-user" id="how-to-copy-user-permissions-from-a-source-to-target-user"></a>

If you are creating a new user and want the new user to have the same permissions as an existing user, you can copy the permissions, instead of assigning them manually.

**To copy the permissions**

1. Navigate to **Set up > User management** and select **Add User**. The **Add New User** page opens.
2. Under **User Details**, provide the email address of the user and their name. Select **Create User and Continue**.
3. Confirm that the user details are correct.
4. Select **Yes** to copy user permissions from another user.
5. Locate the user whose permissions you want to copy and select **Next**. The user's permissions and roles are copied to the new user and a confirmation message is displayed.
6. Under **Review & Edit User**, review the user information and select **Next**.&#x20;
7. Under **Inform User**, choose recipients for the welcome email and select **Complete**.

***

## Updating user permissions

Administrators can edit permissions and security settings for an existing user. &#x20;

**To change user permissions**

1. Navigate to **Set up > User management** and select the user whose permissions you want to edit. Use the search filters to locate the user.&#x20;
2. From the **Actions** column, select **View**. The user's permissions and account settings are displayed.&#x20;
3. Select **Edit** to update the user's information as needed.&#x20;
4. Save your changes when complete.

***

## Deleting users

Administrators can delete a user from the User Management or user details pages.&#x20;

**To delete a user**

1. Navigate to **Set up > User management** and locate the user you want to delete.
2. In the **Actions** column, do one of the following:
   * Select **Delete**.
   * Select **View** and then on the user details page, select **Delete User**.&#x20;
3. Confirm that you want to delete the user.

The user is deleted and a confirmation message is displayed.

***

## Restoring deleted users

Administrators can restore deleted users within 30 days of account deletion. Deleted users can be restored from the User Management or User Details pages.

**To restore a deleted user**

1. Navigate to **Set up > User management** and locate the user you want to restore. Use the search filter to search for deleted users.
2. In the **Actions** column, do one of the following:
   * Select **Restore**.
   * Select **View** and then on the user details page, select **Restore User**.&#x20;

The user is restored and a confirmation message is displayed. The User Management page displays the user status as **Active**, instead of **Deleted**.

***

## Restoring deleted users through the Add Users option <a href="#special-case-restore-users-from-add-users" id="special-case-restore-users-from-add-users"></a>

While creating a new user, a message is displayed if the new user has the same username as the deleted user. Administrators can either restore the deleted user or create a new user with a different user name.

Selecting **Restore User** restores the user with all of their permissions and settings, and changes the user status from **Deleted** to **Active** on the User Management page. &#x20;

<figure><img src="../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure>

***

## Enabling or disabling user access

Administrators can enable user accounts or disable them temporarily. Note that after disabling access, you cannot edit user details or access permissions.&#x20;

**To enable or disable access**

1. Navigate to **Set up > User management** and select the user whose access you want to adjust. Use the search filters to locate the user.&#x20;
2. From the Actions column, select **View**.&#x20;
3. Under **Review & Edit User**, move the slider to change the status based on whether the account is enabled or disabled.
4. In the dialog box, confirm the action.
