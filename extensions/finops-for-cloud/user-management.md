# User Management

The **Users** page in FinOps for Cloud lets you view the current members in your account and invite new ones to join your organization. You can access this page from the sidebar. &#x20;

From this page, you can also remove a member from your account.

## Sending an email invite

Follow these steps to invite new members to your organization:&#x20;

1. On the **Users** page, click **Invite**. The **Invite users** page opens.
2. Enter the details as required:
   1. **Email** - Enter the email addresses of all members you wish to invite. You can invite multiple members at once.
   2. **Role** - Select all the roles you want to assign to the new members. The following options are available:
      * **Organization manager** - This role has the highest level of access and control within the system. It can perform all actions, including inviting new users, changing roles, creating pools and sub-pools, and managing policies such as anomaly detection, quotas, budgets, and tagging. It can also add new data sources and manage all resources within the organization.
      * **Manager** - This role is assigned at the Pool level and can create sub-pools within that pool. It manages resources within their assigned pools, ensuring they are utilized efficiently. The access is limited to the Pool level, and they don't have the same level of control as the Organization Manager. Other functionalities are available in read-only mode.
      * **Engineer** - This role is assigned at the resource level and has read-only access to the other functionalities. Engineers can manage their resources, ensuring they are used efficiently and effectively. However, they can't create new pools or sub-pools.
      * **Member** - Members have read-only access to all system functionalities. They can view information and stay updated on notifications, but they can't make any changes or manage resources.
   3. **Pool** - Specify the pool you want to use. All pools and sub-pools that exist within your environment are displayed. A member with **Manager** and **Engineer** roles can belong to several different pools.
3. Click **Invite** to send the invitation email. Once the invite has been sent, you can view the invitation status on the **Invitations** tab on the **Settings** page.&#x20;

## Deleting users

You can delete a user using the **Delete** icon on the **Users** page.&#x20;

Before deleting, you'll need to choose another user who will take over all the assets of the current user. From the dropdown list, select the required user and then click **Delete** to confirm deletion.&#x20;
