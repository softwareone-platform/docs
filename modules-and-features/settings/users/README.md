---
description: Learn about users in the Marketplace Platform.
---

# Users

A user is an individual who interacts with the platform using a unique username and password.&#x20;

Each user has a profile consisting of attributes and settings (such as email address, name, profile image, and more).

In the SoftwareOne Marketplace, users linked to an account have tailored access to modules and functionalities, depending on their permissions. Users can also belong to multiple accounts or have no account at all:

* Users belonging to multiple accounts can switch between those accounts without signing out of the platform.
* Users who don't belong to any account have limited capabilities. Such users can only sign in to the platform and adjust their profile settings. They cannot access any module.

### Viewing and managing users

Account administrators can view and manage existing users from the **Users** page.

When you launch the page, all users within the account are displayed, allowing you to view each user's details, such as their name, email address, group membership, and the date they last accessed their account.

You can also view the date when they joined the account. If the user has not yet joined, only the invitation status is displayed. Administrators can also view buyers who are visible to the user.

* If the user has access to the **Account Management** module, the column displays **All buyers** as the value. It means that users can view all buyers in the account.
* If the user only has access to the **Marketplace** module, the total number of buyers is shown.
* If the user can only access the **Marketplace** module, the total number of buyers is displayed.
* If the user doesn't have access to either of these two modules, a dash is displayed instead.

The page also contains action links that allow you to edit a user's details or remove them from your account.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Users.png" alt=""><figcaption><p>The Users page in the platform.</p></figcaption></figure></div>

### Viewing user details <a href="#subscription-details" id="subscription-details"></a>

On the user details page, you can view extended information for your selected user.

To open the user  details page:

1. Navigate to the **Users** page.
2. (Optional) Use filters to find the desired user.
3. Select the user to view information, such as the user's name, ID, and email address. You can also check if single sign-on has been enabled for this user.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/settings_user_details_page.png" alt=""><figcaption><p>The details page of a user.</p></figcaption></figure></div>

4. Use the following tabs to access additional related information:&#x20;
   1. **General** - Displays the general user information, such as name and preferences.
   2. **Groups** - Displays the user's group memberships and the modules they have access to.
   3. **Contact entities** - Displays the buyers and licensees mapped to the user. Selecting the buyer or licensee name displays the details page of the selected entity.
   4. **Users** -  Displays all users who are a part of this group.
   5. **Details** - Displays a history of events associated with the user, for example, the date and time when the user was invited to the platform, and so on.
   6. **Audit trail** - Displays a record of events related to the user. For more information, see [Audit Trail](../audit-trail.md).

### Additional actions

You can perform various actions on the **Users** and the **Users' details** pages. The actions available depend on the user's current status:

* [Add New Users](add-new-users.md)
* [Edit user](https://docs.platform.softwareone.com/modules-and-features/settings/users/edit-users)
* [Remove user](https://docs.platform.softwareone.com/modules-and-features/settings/users/remove-user)
* [Manage user invitations](https://docs.platform.softwareone.com/modules-and-features/settings/users/manage-user-invitations)
