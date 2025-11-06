# Buy Perpetual Software Licenses

This tutorial shows how to order a Microsoft [Perpetual Software](../../perpetual-software/) license by setting up a new tenant.&#x20;

Perpetual licenses involve a one-time payment. You pay upfront for these licenses and then use the software indefinitely. In the Marketplace Platform, perpetual licenses can be ordered by creating a purchase order.&#x20;

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you are familiar with the [key concepts](../../../../marketplace-platform/getting-started/key-concepts.md). You will also need:

* A licensee in the **active** state. Licensees are required to set up a new agreement.&#x20;
* Your company details, like the company name, registration ID, and address. These details are required when setting up a new Microsoft tenant.
* The contact details of the person who will manage your Microsoft account.

## Buying Perpetual software licenses <a href="#implementation" id="implementation"></a>

{% stepper %}
{% step %}
{% include "../../../../.gitbook/includes/purchase-wizard-1.md" %}

To start the process:

1. Navigate to the **Products** page.&#x20;
2. Select the required Perpetual Software product, for example, **Microsoft Perpetual Software - Commercial**.
3. On the details page, select **Buy now** to start the ordering process.
{% endstep %}

{% step %}
{% include "../../../../.gitbook/includes/purchase-wizard-2.md" %}

{% include "../../../../.gitbook/includes/in-the-purchase-wizard-com....md" %}

1. **Create agreement** - Select **Create agreement** to start creating your new agreement.
2. **Select licensee** - Choose if you want to use an existing licensee or create a new one. In this tutorial, we'll select an existing licensee. You can add a new licensee by selecting **Add licensee**. For more details, see [Create Licensees](../../../../modules-and-features/settings/licensees/create-licensees.md)
3. **Create agreemen**t - Select **Create new cloud account** to create a new organization tenant with Microsoft, then select **Next**.
4. **Microsoft details** - Provide the following information:
   1. Enter the tenant name you want to use on the onmicrosoft.com domain, then select **Next**. Make sure that the name doesn't include punctuation marks or spaces. You can check whether your tenant name is available using the [Access tenant name availability tool](https://onmicrosoft.platform.softwareone.com/).
   2. Provide the following details:
      1. Company name.
      2. Company registration ID or tax number.
      3. Company address, including city and zip/postal code.
   3. Complete the **Primary Contact** form with the contact details of the person managing your account, then select **Next**.
5. **Special qualifications** - Select the checkbox if your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity. Otherwise, leave it clear. A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
6. **Support contacts** - Enter the contact details of your support administrator and choose your preferred support language. Select **Next**.
7. **Items** - Follow these steps:
   1. Choose the software items you want to order. You can select multiple items.&#x20;
   2. Select **Add items** to add the selected items to your order.&#x20;
   3. Adjust the item quantity as needed, then select **Next**.
8. **Details** - Provide any additional IDs for the order and the agreement, then select **Next**.
9. **Review order** - Read the terms and conditions of the order and the privacy statement. When done, select **Place order**.
10. **Summary** - Select **View details** to go to the order details page. Otherwise, select **Close**.
{% endstep %}
{% endstepper %}

## Next steps <a href="#next-steps" id="next-steps"></a>

Once the order has been placed, we'll verify the order details, including the Microsoft tenant ID.&#x20;

If there are any issues with your order, check the **General** tab on the [order details](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details) page. It will describe the problem and outline the steps you need to follow for us to process your order.

When your order is complete and your license has been set up, you can download your license keys from the [Microsoft admin portal](https://admin.microsoft.com/). For download instructions, see [Download software and product license keys](https://learn.microsoft.com/en-us/microsoft-365/admin/setup/download-software-licenses-csp?view=o365-worldwide#download-software-and-product-license-keys) in Microsoft 365 documentation.
