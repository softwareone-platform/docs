# Order Azure Subscription for Existing Tenant

This tutorial shows how to order a Microsoft Azure subscription by setting up a new agreement and connecting your existing Microsoft tenant.&#x20;

{% embed url="https://vimeo.com/985745743/ebef0c41c4" %}
Video tutorial: How to order Microsoft Azure subscription for an existing tenant
{% endembed %}

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* A licensee in the **active** state or permission to [create a new licensee](../../../modules-and-features/settings/licensees/create-licensees.md) (if you don't want to use an existing licensee). You'll need to select the licensee when setting up the new agreement.&#x20;
* Your Microsoft tenant name.&#x20;
* The contact details of the person who will manage your account.&#x20;

## Ordering an Azure subscription for an existing tenant <a href="#id-1.-launch-the-purchase-wizard" id="id-1.-launch-the-purchase-wizard"></a>

{% stepper %}
{% step %}
{% include "../../../.gitbook/includes/purchase-wizard-1.md" %}

To start the process:

1. Navigate to the **Products** page.&#x20;
2. Select **Microsoft Azure** from the available products.
3. On the details page, select **Buy now**. The purchase process starts.
{% endstep %}

{% step %}
{% include "../../../.gitbook/includes/purchase-wizard-2.md" %}

{% include "../../../.gitbook/includes/in-the-purchase-wizard-com....md" %}

1. **Select agreement** - Select **Create new agreement** to set up a new agreement.
2. **Select licensee** - Choose the licensee you want to use. In this tutorial, we'll select an existing licensee, as shown in the following image. However, you can add a new licensee by clicking **Add licensee** and following the instructions in [Create Licensees](../../../modules-and-features/settings/licensees/create-licensees.md). Select **Next**.&#x20;
3. **Create agreement** - Choose whether you want to create a new Microsoft account or use your existing account, and then select **Next**.  In this tutorial, we'll select **Connect existing cloud account**.
4. **Microsoft details** - Do the following:
   1. (Optional) Select **Access tenant name availability tool** to check the availability of tenant names from Microsoft.
   2. Enter your preferred domain name (also known as the tenant name) in the **Primary** **domain name** field.&#x20;
   3. Fill out the required fields and select **Next**.
5.  **Service level** - Select **Azure Essentials** or **Azure Advanced**, depending on the level of service you require for Azure. In this tutorial, we'll select **Azure Essentials**.&#x20;

    When done, select **Next**.
6. **Service addons** - Select **Next**. Note that when you select **Azure Essentials** or **Azure Advanced**, all add-ons offered as part of the Azure services are displayed. All service add-ons are selected by default, and you cannot change them.&#x20;
7. **Support contacts** - Enter the details of your support admin and select your preferred support language. Then, select **Next**.
8. **Select items** - Select the Azure subscription item and select **Add items** to add it to your order. Note that for Microsoft Azure, there is only one item, with no associated cost. When using Azure services, pay-as-you-go charges are generated against the subscription.
9. **Details** - Enter additional details as required and select **Next**.
10. **Review order** - Review the details of your order and make sure to read the terms using the links in the footer. When done, select **Place order**.
11. **Summary** - Select **View order** to navigate to the order details page. Otherwise, select **Close**.
{% endstep %}
{% endstepper %}

## Next steps

When your order has been placed, we verify the order details and create your new subscription. If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.
