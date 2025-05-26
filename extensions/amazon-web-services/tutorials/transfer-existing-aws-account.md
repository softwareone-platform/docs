# Transfer Existing AWS Account

This tutorial describes how you can transfer your existing AWS accounts to the SoftwareOne Marketplace by establishing a new agreement.&#x20;

## Prerequisites <a href="#prerequisites" id="prerequisites"></a>

Before you start this tutorial, make sure you understand the account transfer options that are available. See [Account Options](../account-options.md) to learn more. Additionally, you'll require the following:

* An active licensee within the Marketplace Platform, or permission to [create a new licensee](https://docs.platform.softwareone.com/modules-and-features/settings/licensees/create-licensees) if you prefer not to use an existing one. Selecting a licensee is required when setting up a new agreement.
* The IDs of the AWS accounts you want to transfer.

## Implementation <a href="#implementation" id="implementation"></a>

{% stepper %}
{% step %}
**Navigate to the Products page**

The **Products** page is located under **Marketplace** in the main navigation menu. The page displays all products available to order from the SoftwareOne Marketplace.
{% endstep %}

{% step %}
**Start the Purchase Wizard for AWS**

From the list of products, select **Amazon Web Services**. Then, on the details page, select **Buy now** to start the purchase wizard.

<figure><img src="../../../.gitbook/assets/aws_productdetails.png" alt=""><figcaption><p>Buy now option on the product details page</p></figcaption></figure>
{% endstep %}

{% step %}
**Follow the steps in the Purchase Wizard**

1. In the **Create agreement** step, select **Create agreement** to start creating your new agreement with SoftwareOne.
2. In the **Select licensee** step, choose if you want to use an existing licensee or create a new one. In this tutorial, we will select an existing licensee. To add a new licensee, select **Add licensee** and follow the instructions in [Create licensee](../../../modules-and-features/settings/licensees/create-licensees.md).
3. In the **Create agreement** step, choose **Existing account**. Then, select **Next**.
4. In the **Existing account** step, choose one of the following options and select **Next**:
   * **Transfer one or multiple accounts without an organization** - Select this option if you have standalone accounts, but not an AWS organization.
   * **Transfer my current AWS organization** - Select this option if you have an AWS master payer account with at least one associated linked account.
   * **Split existing SoftwareOne marketplace agreements** - Select this option if you already have an agreement for AWS through the SoftwareOne Marketplace and want to split the cost among groups of linked accounts. You can do this by creating additional marketplace agreements that are all connected to the same AWS payer account.
5. In the **AWS details** step, do one of the following depending on the selection in the previous step, and select **Next**:

<details>

<summary><strong>Transfer one or multiple accounts without an organization</strong></summary>

If you selected **Transfer one or multiple accounts without an organization** in the previous ste&#x70;**:**

1. Provide your AWS Account ID. Make sure to include all account IDs so we can send the invitation link. After you have accepted the invitation link, we will create an organization and subscriptions on the Marketplace Platform.
2. Review the details under **Notification contact**. By default, this section is prefilled with the information of the selected licensee, who will receive notifications regarding order status.

</details>

<details>

<summary><strong>Transfer my current AWS organization</strong></summary>

If you selected **Transfer my current AWS organization** in the previous step, SoftwareOne Operations will contact you to transfer the payer account of your AWS Organization.

</details>

<details>

<summary><strong>Split existing SoftwareOne marketplace agreements</strong></summary>

If you selected **Split existing SoftwareOne marketplace agreements** in the previous step, do the following to split the costs between licensees:

1. **AWS Master payer ID**: To locate your AWS Master Payer ID, check your existing agreement. Navigate to the **Details** tab on the agreement details page and look under **Additional IDs** to find the **Vendor**. This number is for your master payer account that you want to split.
2. Enter the email that will be used to create your first member account in AWS. Note that this email address must be unique and should not have been used in any other AWS account.
3. Enter a name for the member account you are about to create.
4. By default, the **Notification contact** section is prefilled with the information of the selected licensee to receive notifications regarding order status.

</details>

6. In the **Support level** step, choose a support plan and select **Next**. In this example, we will select **Resold support**. To learn about the support options, see [AWS Concepts](../aws-concepts.md).
7. In the **Items** step, review the details and then select **Next**. This section displays individual items that will be added to your order. To learn more, see My [AWS order contains additional items](../faqs/my-aws-order-contains-additional-items.md).
8. In the **Details** step, provide reference details, like additional IDs or notes, and select **Next**.
9. In the **Review order** step, read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
10. In the **Summary** step, select **View details** to go to the order details page. Otherwise, select **Close** to exit the wizard.
{% endstep %}
{% endstepper %}

## Next steps <a href="#next-steps" id="next-steps"></a>

When your order has been placed, we verify the order details.&#x20;

If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.&#x20;

If you transferred your AWS organization, you'll be contacted by SoftwareOne Operations, who will assist you further in completing the transfer process.

If you transferred standalone accounts, you'll receive invitations for all the accounts specified during the ordering process. To complete this process, you must sign in to each account as an administrator and accept pending invitations on the **Organizations** page within the AWS console.
