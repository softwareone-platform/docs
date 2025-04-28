# User Management

The **Users** page in FinOps for Cloud lets you view the current members in your account and invite new ones to join your organization. You can access this page from the sidebar. &#x20;

From this page, you can also remove a member from your account.

## Sending an email invite

To invite new members to your organization:&#x20;

1. On the **Users** page, select **Invite** to open the **Invite users** page.
2. In **Email**, enter the email addresses of the member you want to invite. You can enter multiple email addresses at once.
3. Select **Add role** to assign a role to the member. The following options are available:
   * **Organization manager** - This role has the highest level of access and control within the system. It can perform all actions, including inviting new users, changing roles, creating pools and sub-pools, and managing policies such as anomaly detection, quotas, budgets, and tagging. It can also add new data sources and manage all resources within the organization.
   * **Manager** - This role is assigned at the Pool level and can create sub-pools within that pool. It manages resources within their assigned pools, ensuring they are utilized efficiently. The access is limited to the Pool level, and they don't have the same level of control as the Organization Manager. Other functionalities are available in read-only mode.
   * **Engineer** - This role is assigned at the resource level and has read-only access to the other functionalities. Engineers can manage their resources, ensuring they are used efficiently and effectively. However, they can't create new pools or sub-pools.
   * **Member** - Members have read-only access to all system functionalities. They can view information and stay updated on notifications, but they can't make any changes or manage resources.
   * **Pool** - Specify the pool you want to use. All pools and sub-pools that exist within your environment are displayed. A member with **Manager** and **Engineer** roles can belong to several different pools.
4. Select **Invite**. &#x20;

An invitation email will be sent to the individual. Once the invite has been sent, you can view the invitation status on the **Invitations** tab within the **Settings** page.&#x20;

## Deleting users

You can delete an individual from FinOps using the **Delete** option on the **Users** page.&#x20;

Before deleting an individual, you must choose another member who will take over all the assets of the individual you want to delete.

To delete an individual:

1. On the **Users** page, locate the individual you want to remove from the account.
2. In the **Actions** column, select the delete icon.
3. In **Delete user**, select the new user who will take over all the assets of the user you want to delete.
4. Select **Delete**.&#x20;
