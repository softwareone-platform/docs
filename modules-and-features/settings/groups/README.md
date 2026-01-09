---
description: Learn about groups in the Marketplace Platform.
---

# Groups

A group represents a set of users who have the same roles and permissions. Groups are used to manage permissions of multiple users at once, instead of at the individual user level.&#x20;

In the Marketplace Platform, users can belong to different groups within the same account. For example, a user can belong to the administrator and finance groups at the same time. They can also have different roles in each account. It means they can be an operations user in one account and an administrator in another.

When working with groups, note the following points:

* Only account administrators can create new groups and manage group details and their members.
* Users must belong to an account before administrators can add them to a group. If the individual doesn't belong to an account, their access to the marketplace platform is restricted.
* Users can belong to multiple accounts and have varying permissions in each, based on their group memberships within each account.

### Viewing groups

To view your existing groups, navigate to the **Groups** page. Only account administrators can access this page.

When you launch the page, all groups in the account are displayed. For each group, you can view details such as the group's name, total number of users it contains, and buyers that are visible to the group members. Buyer visibility is defined by administrators while creating or editing groups. To learn more, see [Restrict Group to Certain Buyers](restrict-group-to-certain-buyers.md).

You can use the [sort and filter options](../../../marketplace-platform/getting-started/interface/customize-the-data-grid.md) to customize the list and [show or hide specific columns](../../../marketplace-platform/getting-started/interface/customize-the-data-grid.md#managing-columns) as needed. Additionally, you can [edit a group](edit-group.md) or [delete it](delete-group.md) using the actions icon (**•••**).

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Groups.png" alt=""><figcaption><p>The Groups page in the platform.</p></figcaption></figure></div>

### Viewing group details <a href="#subscription-details" id="subscription-details"></a>

On the details page of a group, you can view extended information for your selected group.&#x20;

To view the details page for a group:

1. Navigate to the **Groups** page.
2. (Optional) Use filters to find the desired group.
3. Select the group name to view general group information, such as the group name and status.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Groups (1).png" alt=""><figcaption><p>The details page of a group.</p></figcaption></figure></div>

4. Use the following tabs to access additional related information:&#x20;
   * **General** - Displays the group's description.&#x20;
   * **Modules** - Displays modules that are enabled for the group.
   * **Buyers** - Shows buyers enabled for the group. You'll either see details of selected buyers or a message stating that all buyers are enabled, based on your selection during group creation.
   * **Users** -  Displays all users who are a part of this group.
   * **Details** - Displays the event history for the group.
   * **Audit trail** - Displays a record of events related to the group. For more information, see [Audit Trail](../audit-trail.md).

### Additional actions

You can perform various actions on the details page. The available actions depend on the group's status:

* [Edit group](edit-group.md)
* [Delete group](delete-group.md)
* [Restrict groups to certain buyers](restrict-group-to-certain-buyers.md)
