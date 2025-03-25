# Users

A user is an individual who interacts with the In the Marketplace Platform through a unique username and password. Each user has a profile consisting of attributes and settings (such as email address, name,  profile image, and more). To understand more about users and their role in our platform, see [Key Concepts](../../../marketplace-platform/getting-started/key-concepts.md).

Here are some important points about users:&#x20;

* Users can belong to one or more accounts, or none at all.&#x20;
* Users associated with an account have tailored access to modules and functionalities, depending on their permissions.&#x20;
* Users belonging to multiple accounts can also switch between those accounts without signing out of the platform.
* Users who don't belong to any account have limited capabilities. Such users can only sign in to the platform and adjust their profile settings. They cannot access any module.

## Users interface <a href="#agreements-interface" id="agreements-interface"></a>

Account administrators can access the **Users** page by selecting **Settings** > **Users** from the main menu.

<figure><img src="../../../.gitbook/assets/Users.png" alt=""><figcaption><p>Users page</p></figcaption></figure>

The page displays all users in your account. You can [use filters](../../../marketplace-platform/getting-started/interface/customize-the-data-grid.md#filter-data) to search for a user and manage users through the **Actions** column.

For each user, the **Users** page displays the following details:

* **User** - Displays the user's name and their Marketplace identifier.
* **Email** - Displays the email address used to create the account.
* **Joined** - Displays the date when the user accepted the invite.&#x20;
  * If the user accepts the invite and joins your account, the user's status is displayed.&#x20;
  * If the user hasn't accepted the invite, only the invite status is displayed. See [User States](user-states.md) for information on the possible user states.
* **Last sign-in** - Displays the date and time the user signed in to their account.
* **Groups** - Shows the groups that the user belongs to. If the user belongs to multiple groups, the total number of groups is displayed.
* **Modules** - Displays all modules that the user has access to.
* **Buyers** - Displays buyers that are visible to the user.
  * If the user can access the Account Management module, **All buyers** is displayed. Users who can access Account Management can view all buyers in the account.&#x20;
  * If the user can only access the **Marketplace** module, the total number of buyers is displayed.
  * If the user doesn't have access to either of these two modules, a dash - is displayed.
* **Actions** - Displays options that allow you to edit or remove a user from your account.&#x20;

## User details page <a href="#subscription-details" id="subscription-details"></a>

The user details page provides all information for your selected user. You can open the details page by clicking the user name on the **Users** page.&#x20;

<details>

<summary>What can I do on this page?</summary>

From the details page, you can complete the following tasks:&#x20;

* [Edit a user](edit-users.md)
* [Remove a user](remove-user.md)
* [Manage user invitations](manage-user-invitations.md)

</details>

<figure><img src="../../../.gitbook/assets/settings_user_details_page.png" alt=""><figcaption><p>User details page</p></figcaption></figure>

The details page shows all properties associated with the user's profile. It also contains the following tabs:&#x20;

* **General** - Displays the general user details.&#x20;
* **Groups** - Displays the user's group memberships and the modules they have the access to.
* **Contact entities** - Displays the buyers and licensees mapped to the user. Clicking the buyer or licensee name displays the details page of the selected entity.
* **Details** - Displays a history of events associated with the user, for example, the date and time when user was invited to the platform and so on.
* **Audit trail** - Displays a detailed audit trail of all changes. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](https://docs.platform.softwareone.com/modules-and-features/settings/audit-trail).

## Related topics

{% content-ref url="user-states.md" %}
[user-states.md](user-states.md)
{% endcontent-ref %}

{% content-ref url="respond-to-invitations.md" %}
[respond-to-invitations.md](respond-to-invitations.md)
{% endcontent-ref %}

{% content-ref url="add-new-users.md" %}
[add-new-users.md](add-new-users.md)
{% endcontent-ref %}

{% content-ref url="edit-users.md" %}
[edit-users.md](edit-users.md)
{% endcontent-ref %}

{% content-ref url="remove-user.md" %}
[remove-user.md](remove-user.md)
{% endcontent-ref %}

{% content-ref url="manage-user-invitations.md" %}
[manage-user-invitations.md](manage-user-invitations.md)
{% endcontent-ref %}
