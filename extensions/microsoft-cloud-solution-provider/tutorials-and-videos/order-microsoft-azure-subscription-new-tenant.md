# Order Azure Subscription For New Tenant

This tutorial shows how to order a Microsoft Azure subscription by setting up a new agreement and a new Microsoft tenant.

{% embed url="https://vimeo.com/985746673/dda41dd67e" %}
Video tutorial: How to order Microsoft Azure subscription for a new Microsoft tenant
{% endembed %}

## Prerequisites

Before starting this tutorial, make sure you have the following:

* A licensee in the **active** state or permission to [create a new licensee](../../../modules-and-features/settings/licensees/create-licensees.md) (if you don't want to use an existing licensee). You'll need to select the licensee when setting up the new agreement.&#x20;
* Details, such as your company name, registration ID, and address. You'll need to provide these details when creating the new Microsoft tenant.
* Contact details of the person who will manage your account.&#x20;

## Implementation <a href="#id-1.-launch-the-purchase-wizard" id="id-1.-launch-the-purchase-wizard"></a>

{% stepper %}
{% step %}
**Launch the purchase wizard**

Navigate to the **Products** page. Then, select **Microsoft Azure** from the available products.

On the details page, select **Buy now** to start the purchase wizard.

<figure><img src="../../../.gitbook/assets/Azure BuyNow.png" alt=""><figcaption><p>Buy now</p></figcaption></figure>
{% endstep %}

{% step %}
**Complete the steps in the purchase wizard**

1. In the **Create agreement** step, choose **Create agreement** to start creating your new agreement.
2. In the **Select licensee** step, choose if you want to use an existing licensee or create a new one. In this tutorial, we'll select an existing licensee. You can add a new licensee by selecting **Add licensee**. See [Create Licensees](../../../modules-and-features/settings/licensees/create-licensees.md) for instructions.
3. In the **Create agreement** step, select **Create new cloud account** to create a new organization tenant with Microsoft. Then, select **Next**.
4. In the **Microsoft details** step, enter the details for your Microsoft account:
   1. Enter the tenant name you want to use on the onmicrosoft.com domain. Make sure that the name doesn't include punctuation marks or spaces. You can check whether your tenant name is available using the [Access tenant name availability tool](https://onmicrosoft.platform.softwareone.com/).
   2. Select **Next**. The platform validates the details that you entered.
   3. Fill out the contact form. You'll need to provide the following details:
      1. Company name.
      2. Company registration ID or tax number.
      3. Company address, including city and zip/postal code.
      4. Contact details of the person who will manage your account.&#x20;
5. Select **Next**. In the **Service level** step, select **Azure Essentials** or **Azure Advanced**, depending on the level of service you require for Microsoft Azure. Select **Next**.
6. In the **Service add-ons** step, all add-ons offered as part of the Azure services are displayed. These are selected by default, and you cannot change them. Select **Next**. &#x20;
7. In the **Support contacts** step, enter the contact details of your support administrator and choose your preferred support language. When done, select **Next**.
8. In the **Items** step, choose the Azure subscription and select **Add items** to add it to your order. Note that for Microsoft Azure, there is only one item, with no associated cost. When using Azure services, pay-as-you-go charges are generated against the subscription.

<figure><img src="../../../.gitbook/assets/azure_select_items.png" alt=""><figcaption><p>Select Items</p></figcaption></figure>

9. In the **Details** step, provide reference details, like additional IDs or notes, and select **Next**.
10. In the **Review order** step, read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
11. In the **Summary** step, select **View details** to go to the order details page. Otherwise, select **Close** to exit the wizard.
{% endstep %}
{% endstepper %}

## Next steps

When your order has been placed, we verify the order details and create your new subscription. If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.
