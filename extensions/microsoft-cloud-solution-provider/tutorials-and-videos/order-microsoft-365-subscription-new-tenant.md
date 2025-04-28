# Order Microsoft 365 Subscription For New Tenant

This tutorial guides you through the steps to order a Microsoft 365 subscription by creating a new agreement.

When establishing a new agreement with SoftwareOne, you can either establish a new Microsoft account or use an existing one. In this tutorial, you'll be setting up a new Microsoft account.&#x20;

{% embed url="https://vimeo.com/985743941/17387d808a?share=copy" %}
Video tutorial: How to order Microsoft 365 subscription for a new tenant
{% endembed %}

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* A licensee in the **active** state, or permission to [create a new licensee](../../../modules-and-features/settings/licensees/create-licensees.md) if you don't want to use an existing active licensee. Licensee selection is required when setting up a new agreement.&#x20;
* Your company details, like the company name, registration ID, and address. These details are required for creating a new Microsoft tenant.&#x20;
* The contact details of the person who will manage your Microsoft account.&#x20;

## Implementation

{% stepper %}
{% step %}
**Launch the purchase wizard**

Navigate to the **Products** page. Then, select **Microsoft 365 Business, Enterprise & Apps - Commercial** from the available products.

On the details page, select **Buy now** to start the purchase wizard.
{% endstep %}

{% step %}
**Complete the steps in the Purchase wizard**

1. In the **Create agreement** step, select **Create agreement** to start creating your new agreement.
2. In the **Select licensee** step, choose if you want to use an existing licensee or create a new one. In this tutorial, we'll select an existing licensee. You can add a new licensee by selecting **Add licensee**. See [Create Licensees](../../../modules-and-features/settings/licensees/create-licensees.md) for instructions.
3. In the **Create agreemen**t step, select **Create new cloud account** to create a new organization tenant with Microsoft. Then, select **Next**.
4. In the **Microsoft details** step, enter the details for your Microsoft account:
   1. Enter the tenant name you want to use on the onmicrosoft.com domain. Make sure that the name doesn't include punctuation marks or spaces. You can check whether your tenant name is available using the [Access tenant name availability tool](https://onmicrosoft.platform.softwareone.com/).
   2. Select **Next**. The platform validates the details that you entered.
   3. Fill out the contact form and select **Next**. You'll need to provide the following details:
      1. Company name.
      2. Company registration ID or tax number.
      3. Company address, including city and zip/postal code.
      4. Contact details of the person who will manage your account.&#x20;
5. In the **Special qualifications** step, select the checkbox if your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity. Otherwise, leave it clear. A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
6. In the **Support contacts** step, enter the contact details of your support administrator and choose your preferred support language. Select **Next**.
7. In the **Items** step, do the following:
   1. Choose the items you want to order. You can select multiple items. Then, select **Add items.**&#x20;
   2. Review and adjust the number of licenses as required.
   3. If applicable, [read the offer attestation](../faqs/what-is-offer-attestation.md). The offer attestation is only displayed for Windows 365 Business with the Windows Hybrid Benefit.&#x20;
   4. Select **Next**.
8. In the **Details** step, provide reference details, like additional IDs or notes, and select **Next**.
9. In the **Review order** step, read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
10. In the **Summary** step, select **View details** to go to the order details page. Otherwise, select **Close** to exit the wizard.
{% endstep %}
{% endstepper %}

## Next steps

When your order has been placed, we verify the order details, including the Microsoft tenant ID, and create your new subscription. If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.
