---
description: Administrators can set up multi-step approval workflows for purchasing.
---

# Setting Up and Using Approval Workflows

***

### Creating an approval group

You can create up to 3 levels of purchase approval groups.

**To create an approval group**

1. From the main navigation menu, navigate to **Setup** and select **Purchase Approval Setup**.
2. Select **New Group**. The Create Approval Group window opens.
3. Provide a name for your approval group, select the approval level, and log in from the list.
4. Select **Create** to create the approval group.

If an order created by the user exceeds the allowed spending limit, the individuals in the approval group will be listed as valid approvers. These approval groups can be linked together by creating parent-child relationships.

***

### Creating an approval workflow

The **Purchase Approval Setup** page displays a list of all users that have access to the Client Portal.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

**To set up an individual workflow/approval for a user**

1. In the **Actions** column, select **Approval Workflow Setup**.
2. On the Approval Workflow Setup page, provide the required information:

| Field                       | Description                                                                                                                                                                                                                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Purchase Approval Group** | Indicates the group that will approve the user’s transaction when approval is required.                                                                                                                                                                                                                 |
| **Currency**                | Indicates the currency on which the rule will apply. If you select **Any**, the rule applies to all currencies.                                                                                                                                                                                         |
| **Publisher**               | Allows you to select a publisher if you want to create a workflow role for a specific publisher. If you select **Any**, the workflow rules will apply to all.                                                                                                                                           |
| **Total Amount**            | Defines the limit to which amount a user can purchase without approval. This is defined based on the currency, and manufacturer, where manufacturers are possible wild cards. If the user makes any transaction that exceeds the amount, approval is required from the selected purchase approval group |

3. Select **Create Rule** and then click on **Save** to save the new rule.

***

### Deleting a rule

**To delete an existing rule**

1. On the Purchase Approval Setup page, select the user. The Approval Workflow Setup window opens.
2. In the **Actions** column, select **Delete**.

<figure><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Select **Yes** to delete the rule.
