---
description: Learn about groups in the Marketplace Platform.
---

# Groups

A group represents a set of users who have the same roles and permissions. Groups are used to manage the permissions of multiple users at once, instead of at the individual user level.&#x20;

In the Marketplace Platform, users can belong to different groups within the same account. For instance, a user can belong to the administrator and finance groups at the same time. They can also have different roles in each account, for instance, being an operations user in one account and an administrator in another.

When working with groups in the platform, note the following points:

* Only account administrators can create new groups and manage group details and their members.
* Users must belong to an account before administrators can add them to a group. If the individual doesn't belong to an account, their access to the marketplace platform is restricted.
* Users can belong to multiple accounts and have varying permissions in each, based on their group memberships within each account.

Account administrators can view their groups on the **Groups** page.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Groups.png" alt=""><figcaption><p>The Groups page in the platform.</p></figcaption></figure></div>

The page shows all groups in the account. For each group, you can view details such as the group's name, total number of users it contains, and buyers that are visible to the group members. Buyer visibility is defined by administrators while creating or editing groups. To learn more, see [Restrict Group to Certain Buyers](restrict-group-to-certain-buyers.md).

You also have options that [edit a group](edit-group.md) or [delete it](delete-group.md) using the actions icon (**•••**).

## Viewing group details <a href="#subscription-details" id="subscription-details"></a>

To view the details page of a group, select the group on the **Groups** page.&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Groups (1).png" alt=""><figcaption><p>The details page of a group.</p></figcaption></figure></div>

The group details page contains general group information, such as group name and status. It also contains the following tabs:

<table><thead><tr><th width="144">Tab</th><th>Description</th></tr></thead><tbody><tr><td><strong>General</strong></td><td>Displays the group's description. </td></tr><tr><td><strong>Modules</strong></td><td>Displays modules that are enabled for the group.</td></tr><tr><td><strong>Buyers</strong></td><td>Shows buyers enabled for the group. You'll either see details of selected buyers or a message stating that all buyers are enabled, based on your selection during group creation.</td></tr><tr><td><strong>Users</strong></td><td> Displays all users who are a part of this group.</td></tr><tr><td><strong>Details</strong></td><td>Displays the event history for the group.</td></tr><tr><td><strong>Audit trail</strong></td><td>Displays an audit trail of all changes and events within the group. For each audit record, you can view the log details and summary. To learn more, see <a href="../audit-trail.md">Audit Trail</a>.</td></tr></tbody></table>

## Additional actions

You can perform various actions on the details page. The available actions depend on the group's status:

* [Edit group](edit-group.md)
* [Delete group](delete-group.md)
* [Restrict groups to certain buyers](restrict-group-to-certain-buyers.md)
