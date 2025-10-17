# Create New AWS Account

This tutorial describes how to create a new AWS account by establishing a new agreement with SoftwareOne.&#x20;

When setting up a new agreement, you can either set up a new AWS account or transfer your existing AWS account. In this tutorial, you'll create a new AWS account.

## Prerequisites <a href="#prerequisites" id="prerequisites"></a>

Before starting this tutorial, make sure that you are familiar with the concepts and support models in[ AWS concepts](../aws-concepts.md). You'll need to choose the support level when creating your new account.

Additionally, you'll require the following:

* An active licensee within the Marketplace Platform, or permission to [create a new licensee](https://docs.platform.softwareone.com/modules-and-features/settings/licensees/create-licensees) if you prefer not to use an existing one. Selecting a licensee is required when setting up a new agreement.
* The email address of your root user and the name of your AWS account.
* The contact details of the person who will manage your AWS account. We'll send notification emails and account invitations to this assigned contact person.&#x20;

## Creating a new AWS account

{% stepper %}
{% step %}
**Start the purchase wizard for AWS**

To start the wizard:

1. Navigate to the **Products** page.
2. From the list of products, select **Amazon Web Services**.&#x20;
3. On the product details page, select **Buy now**. The Purchase Wizard for AWS starts.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/aws_productdetails.png" alt=""><figcaption><p>Buy now option on the product details page</p></figcaption></figure></div>
{% endstep %}

{% step %}
**Follow the wizard to create a new AWS account**

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/aws_purchase_wizard.png" alt=""><figcaption><p>Purchase wizard for AWS</p></figcaption></figure></div>

Complete the following steps, making sure to enter or verify the required information where necessary:

1. **Select agreement** - Select **Create agreement** to start creating your new agreement with SoftwareOne.
2. **Select licensee** - Choose if you want to use an existing licensee or create a new one. In this tutorial, we will select an existing licensee. To add a new licensee, select **Add licensee** and follow the instructions in [Create licensee](../../../modules-and-features/settings/licensees/create-licensees.md).
3. **Create agreement** - Choose **New account** to create a new organization with AWS. Then, select **Next**.
4. **AWS details** - Provide the necessary information:
   1. **Email** - Enter the email address you want to use for this member account in AWS. Make sure that the email address is unique and hasn't been used previously in the AWS cloud.&#x20;
   2. **Account name** - Enter a name for the new account.
   3. **Notification contact** - Review the contact details. These details are prepopulated with the details of your selected licensee. The contact listed in this section will receive all account-related notifications, including account invitations.&#x20;
5. **Service level** - Select **Next**. This page displays all services you get as part of your agreement. It's not possible to change these options.
6. **Support info** - Choose a support plan and select **Next**. In this example, we'll select **Resold support**. Learn about the support options in [AWS Concepts](../aws-concepts.md).

{% hint style="info" %}
Choose your support type carefully, as it will affect the deployed guardrails, pricing, and the tasks required after creating your AWS account and Marketplace agreement. Once you select a support type, changing it involves a manual process and is currently not supported by the SoftwareOne Marketplace.
{% endhint %}

7. **Items** - Check the items in your order and select **Next**. Note that these items are added by default and can't be removed. To learn more, see [My AWS order contains additional items](../faqs/my-aws-order-contains-additional-items.md).
8. **Details** - Provide reference details, like additional IDs or notes. Then, select **Next**.
9. **Review order** - Read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
10. **Summary** - Select **View details** to go to the order details page. Otherwise, select **Close**.
{% endstep %}
{% endstepper %}

## Next steps <a href="#next-steps" id="next-steps"></a>

When your order has been placed, we verify the order details.&#x20;

If there are issues with your order, for example, if the email address you provided is incorrect or already in use, the [order details](../../../modules-and-features/marketplace/orders/#subscription-details)[ ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and the actions you need to take.&#x20;

If there are no issues, we'll create an AWS account using the name and email address you provided. You'll receive an email with instructions on resetting your password and accessing your account.

{% hint style="info" %}
Make sure to save your login credentials for future reference. SoftwareOne does not keep a copy of your email and password.
{% endhint %}

After signing in, you can start deploying AWS resources. See the AWS documentation and best practices for guidance on deploying and managing your resources.&#x20;

If you selected **Resold support** during the ordering process, you'll need to add your support plan to the AWS console. To do this, go to your AWS console's account settings and select the desired [AWS support level](https://docs.aws.amazon.com/awssupport/latest/user/aws-support-plans.html). Note that enrolling in AWS support will incur monthly charges as described at [AWS Support Plan Pricing](https://aws.amazon.com/premiumsupport/pricing/).
