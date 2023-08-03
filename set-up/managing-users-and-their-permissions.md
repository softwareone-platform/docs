---
description: Manage users and define user permissions through the User Management module.
---

# Managing users and their permissions

The User Management module allows administrators to perform the following tasks:

* Create new users
* Change user security settings
* Manage user feature privileges
* Manage user access to Spend Management
* Access or request user procurement settings
* Manage user access to Collaboration Site folders
* Block or enable access to the SoftwareOne Client Portal

***

### Accessing the User Management module

Only the users that have administrator privileges can access User Management. Administrator privileges are set up for your specified users during onboarding.

**To access the User Management module**

* From the main navigation menu, navigate to **Setup** and select **User Management**.

***

### Creating a new user

**To add a user**

1\. Select **Add User** on the User Management page.

2\. On the **Add New User** page, perform the following steps:

* Provide the first name, last name, and email address of the user.
* Choose whether you want to apply administrator permissions or basic user permissions.

3\. Select the Procurement Settings check box if you want the user to have access to your procurement setting and then fill out the Procurement Settings section. This section is displayed only after you select the check box.

4\. Select **Save Changes**.

A welcome email with the login details is sent to the new user.

***

### Updating the user permissions

You can edit the permissions and the security settings for a user. &#x20;

**To change a user's permissions**

1\. Select **Edit User** to change the security settings.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/09/User-Management-v1_05-Edit-User-1024x466.png" alt=""><figcaption></figcaption></figure>

2. Edit the permissions and the security settings. You cannot edit the name and email address.
3. Select **Save Changes.**&#x20;

***

### Viewing the list of features users can access

Select the **Feature** tab on the User Details page to view user permissions.

To grant or remove access to a feature, enable or disable a selected feature, and specify the roles to be assigned to that user.

***

#### Unable to grant permission?

If you're unable to provide access to a selected feature or select a specific role, it might be because of the following reasons:

* The user has no Procurement Permissions set up. To resolve this, request Procurement Permissions for this user. The feature will become available after these permissions are provided.
* The roles) are read-only. To resolve this issue, contact our Support team because there might be an issue with the legacy access configuration.

***

### Configuring spend management access

User Management provides extensive capabilities to define user data access for Spend Management. It is possible to limit user access by Accounts or Custom Groups.

Users can limit access by choosing the **Spend Management Access** tab.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-180-1024x547.png" alt=""><figcaption></figcaption></figure>

***

### Providing full access

Select **Full Access** to give users full access to all Spend Management data.

{% hint style="info" %}
**Note:** By default, each user has full access.
{% endhint %}

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-181-1024x547.png" alt=""><figcaption></figcaption></figure>

***

### Limiting user access by accounts

Choose **Accounts** to use existing Providers and Subscriptions to configure access. Select **Next** to define the access.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-185-1024x495.png" alt=""><figcaption></figcaption></figure>

Choose whether the user will be able to access the following data:

* Any Account out of existing Providers
* Selected Cloud Accounts (Tenants)
* Selected Subscriptions

{% hint style="info" %}
**Note**: Defining access on the Provider level gives access to all Accounts and Subscriptions including those added in the future. Users will get access to new entities automatically. The same rule applies for defining access on the Account (Tenant) level.
{% endhint %}

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-184-1024x650.png" alt=""><figcaption></figcaption></figure>

Save your changes in order to make the changes effective.

***

### Limiting user access by custom groups

1. Choose **Custom Groups** to give users access only to selected groups. Select **Next**.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-186-1024x503.png" alt=""><figcaption></figcaption></figure>

</div>

2. Choose the groups the user can access. Selecting a group (or a branch) will allow the user to see all resources assigned to that group, and all cloud spend data related to those resources.

{% hint style="info" %}
**Note:** Giving access to a parent group will allow the user to access the parent and all its children groups.
{% endhint %}

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/07/word-image-11.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

3. Select **Save**.

***

### Accessing user procurement settings

Choose the **Procurement** tab to open the current user Procurement settings.&#x20;

You will see all the countries where the user can procure. Choose a country to see and manage permissions. You must own sufficient privileges to edit the permissions (some of them may appear read-only). The privileges may be different depending on the country.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-188-1024x774.png" alt="" width="563"><figcaption></figcaption></figure>

</div>

***

### Requesting procurement settings

Newly created users will not have Procurement Settings provided. Users need to be defined to transact through PyraCloud, therefore it may not be possible to enable some of the features for such users.

You can request for these users to be configured. First, choose the **Procurement** tab and click on the **Request Procurement** option.

The Procurement Request form will be displayed. Fill in the information and confirm by clicking the "Request Procurement" option. The request will be processed by a SoftwareOne sales representative.

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-43-671x1024.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

***

### Managing access to the Collaboration Site folders

You can manage user access to folders existing in the Collaboration Site. Select the **Collaboration Site** tab on the user details page.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/10/image-189-1024x365.png" alt="" height="238" width="668"><figcaption></figcaption></figure>

Selected folder access configuration will be immediately reflected in the Collaboration Site.

***

### Disabling user access

**To disable access**

1. Select the **Disable User** option. A confirmation message is displayed.&#x20;
2. Select **Disable** to confirm the action.

After you disable a user, they will no longer be able to sign in.&#x20;

<div align="left">

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/09/User-Management-v1_13-Disable-User-1024x474.png" alt=""><figcaption></figcaption></figure>

</div>
