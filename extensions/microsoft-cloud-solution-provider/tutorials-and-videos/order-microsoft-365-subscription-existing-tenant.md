# Order Microsoft 365 Subscription For Existing Tenant

This tutorial guides you through the steps to order a Microsoft 365 subscription by creating a new agreement.

When establishing a new agreement with SoftwareOne, you can either establish a new Microsoft account or use an existing one. In this tutorial, you'll connect your existing cloud account.&#x20;

{% embed url="https://vimeo.com/985744841/f08189d1c0" %}
Video tutorial: How to order Microsoft 365 subscription for an existing tenant
{% endembed %}

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* Your Microsoft tenant name.&#x20;
* A Marketplace licensee in the **active** state or permission to [create a new licensee](../../../modules-and-features/settings/licensees/create-licensees.md) (if you don't want to use an existing licensee). You'll need to select the licensee when you are creating the agreement.&#x20;

## Implementation

{% stepper %}
{% step %}
**Launch the purchase wizard**

Navigate to the **Products** page on the platform. Then, select **Microsoft 365 Business, Enterprise & Apps - Commercial** from the available products.

On the details page, select **Buy now** in the upper right to start the purchase wizard.
{% endstep %}

{% step %}
**Complete the steps in the purchase wizard**

1. In the **Create agreement** step, select **Create agreement** to start creating your new agreement.
2. In the **Select licensee** step, choose if you want to use an existing licensee or create a new one. In this tutorial, we'll select an existing licensee. You can add a new licensee by selecting **Add licensee**. See [Create Licensees](../../../modules-and-features/settings/licensees/create-licensees.md) for instructions.
3. In the **Create agreemen**t step, select **Connect existing cloud account** to connect your existing tenant. Then, select **Next**. Note that if you choose this option, the global administrator of your Microsoft account will need to accept the relationship request.
4. In the **Microsoft details** step, enter the details for your Microsoft account:
   1. Enter the name of your existing tenant.
   2. Fill out the contact form. You'll need to provide the first and last name, email address, and phone number of the person who will manage your account.&#x20;
   3. Select **Next**. The platform will validate your Microsoft tenant details. If no tenant is found, a message is displayed. You'll need to fix the error to proceed.
5. In the **Special qualifications** step, select the checkbox if your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity. Otherwise, leave it clear. A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
6. In the **Support contacts** step, enter the contact details of your support administrator and choose your preferred support language. Select **Next**.
7. In the **Items** step, do the following:
   1. Choose the items you want to order and then select **Add items**. You can select multiple items. When the items are added, the **Select items** section is displayed.
   2. Review and adjust the license quantity as required.
   3. If applicable, [read the offer attestation](../faqs/what-is-offer-attestation.md). The offer attestation is only displayed for Windows 365 Business with the Windows Hybrid Benefit.&#x20;
   4. Select **Next**.
8. In the **Details** step, provide reference details, like additional IDs or notes, and select **Next**.
9. In the **Review order** step, read the terms and conditions and the privacy statement. When done, select **Place order**.
10. In the **Summary** step, select **View details** to go to the order details page; otherwise, select **Close** to exit the wizard.
{% endstep %}
{% endstepper %}

## Next steps

Once you have placed your order, we'll verify the order details, including the Microsoft tenant ID, and create your new subscription under your existing tenant. If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.
