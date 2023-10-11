# How to manage users using the User Management wizard

The new version of User Management is currently available for most PyraCloud customers. If you cannot see the User Management wizard, then SoftwareONE will need to migrate your data first.

### Introduction <a href="#post-4972-_ref61592726" id="post-4972-_ref61592726"></a>

The User Management feature is available to all PyraCloud customers. It allows PyraCloud Administrators to do the following:

* Add new users
* Change account security settings
* Manage feature permissions
* Manage user access to companies\*
* Manage user access to Spend Management\*
* Manage user access to Collaboration Site folders\*
* Disable users to block their access to PyraCloud
* Delete PyraCloud users

\*… this functionality only applies to certain PyraCloud features.

### Access User Management <a href="#post-4972-_toc62223014" id="post-4972-_toc62223014"></a>

The User Management feature can only be accessed by users that have admin privileges. Admin privileges are set up for your specified users during the PyraCloud onboarding process.

In order to access User Management click on “Setup” > “User Management” as shown below:

### Browse User List <a href="#post-4972-_toc62223015" id="post-4972-_toc62223015"></a>

The User Management main page shows a complete list of PyraCloud users. The following user information is displayed:

* Username
* E-mail
* Last Login Date
* User Type
* User Status

Click on “View” in the “Actions” column to view summary information for that user (see details in Review & Edit User).

### Search for a User <a href="#post-4972-_toc62223016" id="post-4972-_toc62223016"></a>

Use the search field to search for a specific user. Simply type the user name or email address to filter the user list.

### Add a User <a href="#post-4972-_toc62223017" id="post-4972-_toc62223017"></a>

Choose “Add User” to add a PyraCloud user.

Then follow the steps shown in the User Management Wizard to define the user. These steps are documented in the User Management Wizard section below.

### User Management Wizard <a href="#post-4972-_toc62223018" id="post-4972-_toc62223018"></a>

User Management has a wizard that guides you through the process of adding a PyraCloud user. The same structure is also used to edit an existing PyraCloud user.

The steps are shown in 3 different visual ways depending on their status:

* **Green number** – these are steps which can be done
* **Gray** – these are steps which can only be done once another step has been completed. The step number and name of the step is grayed out
* **Green tick** – steps which are done are ticked off in green. That means that a User Management administrator has explicitly saved this step at least once.

The name of the active step is displayed in bold.

### User Details <a href="#post-4972-_toc62223019" id="post-4972-_toc62223019"></a>

Specify the following for the user:

* E-mail address
* First name
* Last name

After you click on “Save and Continue”, confirm that your entered data is correct:

### Copy User <a href="#copy-user" id="copy-user"></a>

After the user has been created, select if you want to create the user by copying from an existing user:

* Click on “Yes” to select a user to copy from
* Click on “No, Thanks” to continue to manually add the user

If the user can be created by copying from an identical or similar user, select the user to copy from. Search for the user to find it, select it and click on “Next”:

After clicking on “Next”, all permissions and settings for the new user will be copied from the selected user. Review the user on the “Review and Edit User” page. If required, change the permissions and settings of the new user.

### Account Security <a href="#account-security" id="account-security"></a>

Continue to manually add the user by specifying the account security settings if they required:

* **Multi-Factor-Authentication (MFA) after inactivity:** If the user has not logged on for a specified number of days, they are required to use a second factor before they can login to PyraCloud again.
* **Multi-Factor-Authentication (MFA) for every login:** Users are required to use a second factor for every login to PyraCloud. This setting is enabled by default.
* **Automated account blocking:** If the user has not logged on for a specified number of days, then they are automatically blocked and cannot login to PyraCloud before being unblocked.
* **Password expiration:** Number of days after which they user must change their password. This setting can only be specified for users who login to PyraCloud with a username and password.

### Feature Permissions <a href="#post-4972-_ref61616565" id="post-4972-_ref61616565"></a>

Specify which PyraCloud features the user is allowed to use in this step:

* **Select the user type**
  * PyraCloud Administrators have access to User Management and can manage users and their access
  * Users do not have access to User Management
* **Enable feature permissions for a user**
  * Select a role to assign a set of predefined permissions
  * Click on “Show All Permissions” to browse the list of permissions or search for the permissions
  * Use the toggle to grant or revoke permissions. If used on feature level, it will grant or revoke all permissions of the feature
  * The toggle will only apply to the search results

The “Procurement (excluding Office365)” role is visible for all PyraCloud customers and can be used by all PyraCloud Administrators. Other roles will only be visible if customers have purchased the corresponding service from SoftwareONE.

Click on the role again to disable the role and their predefined permissions. Click on enabled permissions to disable them. This might add the text “edited” at the end of the role to indicate that only some permissions of the role are enabled.

* If an “i” icon is displayed next to a permission, hover over the icon to read a more detailed description.

**Note:** User Management Administrators can only give users access to features which their own user has. This is the reason why User Management Administrators cannot manage the feature permissions of their own user. If they removed feature permissions from their user, then they would not be able to give access to those permissions to other PyraCloud users anymore.

### Company Access <a href="#post-4972-_toc62223022" id="post-4972-_toc62223022"></a>

Manage the companies for which users get access to in this step. The “Company Access” step is only available when a permission is enabled for a user that requires them to define the company access, e.g. procurement.

Click on the checkbox to grant users access to a folder:

Grant access to the complete company structure by clicking on the checkbox of the folder at the top. Alternatively, grant access to any part of the company structure.

Grant different access in the following order:

| State of Checkbox                                                                                               | Description                                                                                                                                                                                                    |
| --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://help.pyracloud.com/wp-content/uploads/2021/02/word-image-52.png" alt="" data-size="original"> | Users do not have access to companies in that folder nor any sub-folder                                                                                                                                        |
| <img src="https://help.pyracloud.com/wp-content/uploads/2021/02/word-image-53.png" alt="" data-size="original"> | Users have access to all companies in that folder and all sub-folders. Users will automatically have access to any companies that are added to these folders or as separate sub-folders in the future.         |
| <img src="https://help.pyracloud.com/wp-content/uploads/2021/02/word-image-54.png" alt="" data-size="original"> | Users have access to all companies in that folder and to some sub-folders. Users will NOT have automatically access to any companies that are added to these folders or as separate sub-folders in the future. |

### Procurement Settings <a href="#post-4972-_toc62223023" id="post-4972-_toc62223023"></a>

In this step you can specify additional procurement settings. It is only available when at least one permission of the “Procurement” feature is enabled for the user and the user has access to at least one company.

Fill out the required data fields.

**Note:** The procurement settings are specific for the SoftwareONE legal entities. If users can purchase from SoftwareONE Finland and SoftwareONE Inc., then the users can have different settings for those 2 SoftwareONE legal entities.

Hover over the “i” icon to read a more detailed description for each procurement setting.

### Catalog and Documents <a href="#catalog-and-documents" id="catalog-and-documents"></a>

In this step you can restrict from which SoftwareONE legal entities your users can purchase for their companies. It also limits the access to documents like quotes, orders and invoices by SoftwareONE legal entities. It is only available when at least one permission of the “Procurement” feature is enabled for the user and the user has access to at least one company.

By default, users can purchase from all SoftwareONE legal entities and have access to all documents of their companies.

Restrict the user access by clicking on the “Limit Access to Catalog and Documents by SoftwareONE Entities” toggle and select the SoftwareONE legal entities for which the user needs access. If required, use the search to limit the number of legal entities.

### Spend Management Access <a href="#post-4972-_toc62223024" id="post-4972-_toc62223024"></a>

User Management provides extensive capabilities to define user data access for Spend Management in PyraCloud. It is possible to limit user access by Accounts or Custom Groups. This step is only available when permissions for a “Spend Management” feature is enabled for the user.

Specify the level of access for the user to the Spend Management data:

1. **Full Access:** Users can access all data without any restrictions. Every user has full access by default.
2. **Accounts:** Users can access the data for all granted providers and subscriptions
3. **Custom Groups:** Users can access the data for all granted custom groups

“Full Access” is already selected. If required, select it and click on “Save and Continue”

1. Accounts

* Click on the “Accounts” radio button
* Click “Next”
* Specify for which providers, tenants and / or subscriptions the user needs access.

**Note:** If users have access on the “Provider” level, then they have access to all tenants and subscriptions of that provider (including those added in the future).

* Click on “Save and Continue”

2\. Custom Groups

* Click on the “Custom Groups” radio button
* Click “Next”
* Specify for which group(s) the user needs access.

**Note:** User will be able to see all resources assigned to the assigned groups, and all Spend Management data related to those resources.

**Note**: When users have access to a “parent” group, then they have access to the “parent” and all its “child” groups.

* Click on “Save and Continue”

### Collaboration Site Access <a href="#post-4972-_toc62223025" id="post-4972-_toc62223025"></a>

In this step you can manage the user access to folders which exist in the Collaboration Site. It is only available when a “Collaboration Site” permission is enabled for the user.

* Specify the level of access for the user for each Collaboration Site folder
* Click on “Save and Continue”

Specify the following:

* **None:** Users cannot access these folders
* **Read:** Users can access files in these folders but they cannot change or upload files
* **Read, Write:** Users have full access to these folders

### Review and Edit User <a href="#post-4972-_ref61614954" id="post-4972-_ref61614954"></a>

This step shows a summary of the user for you to review.

* It shows a limited view of what is enabled for the “Feature Permissions” and “Company Access” steps and
* A summary with numbers for all other steps, e.g. x / y account security settings are enabled

This is the last step before informing the new users about their PyraCloud access or the starting point when viewing existing users.

Click on “Edit” for one of the sections, or click on the step in the wizard to update the user.

### Inform User <a href="#post-4972-_toc62223027" id="post-4972-_toc62223027"></a>

You are now ready to inform new users about their access to PyraCloud.

The PyraCloud welcome e-mail can only be sent once and the step will no longer be shown in the User Management wizard.

If users delete or lose their PyraCloud welcome e-mail, they can go to the PyraCloud login page where they can click on the “Don’t remember your password?” link to reset their password

**Note:** If User Management administrators want to hand-over PyraCloud credentials to their users later (e.g. after an introduction meeting), then they can either wait with the “Inform User” step or send the welcome e-mail to themselves and forward it separately.
