# How to Order Products for Reselling

The tutorial describes how you can order products for reselling through the Marketplace Platform.&#x20;

When ordering products, there are two options for agreements:

* If you have an existing agreement, you can use that agreement. However, you'll need to make sure that the agreement is mapped to a licensee configured for reselling. If the agreement doesn't have a resale licensee, the transaction won't be allowed.
* If you don't have an agreement, you can create one during the ordering process and select an existing licensee you've configured for reselling.

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* A **resale** licensee in the **active** state, or permission to [create a new licensee](how-to-configure-licensees-for-resale.md) if you don't want to use an existing licensee. Licensee selection is required when setting up a new agreement.&#x20;
* Company details of your client, like the company name, registration ID, and address. These details are required for creating a new Microsoft tenant.&#x20;
* The contact details of your client who will manage the Microsoft account.&#x20;

## Implementation

{% stepper %}
{% step %}
**Navigate to the Products page**

The **Products** page is located under **Marketplace** in the main navigation menu. The page displays all products available to order from the SoftwareOne Marketplace.
{% endstep %}

{% step %}
**Start the Purchase Wizard for Microsoft 365**

From the list of products, select **Microsoft 365 Business, Enterprise & Apps - Commercial**. Then, on the details page, select **Buy now** to start the purchase wizard.

<figure><img src="../../../.gitbook/assets/MS365BuyNow.png" alt=""><figcaption><p>Buy now option on the details page</p></figcaption></figure>
{% endstep %}

{% step %}
**Use the Purchase Wizard to order licenses**

Complete all steps in the wizard, making sure to enter or verify the required information on each page.

1. **Select agreements** - Select **Create agreement** to start creating your new agreement.
2. **Select licensee** - Choose a licensee from the list.  Make sure that the **Resale** column for the licensee displays **Yes**. Then, select **Next**.&#x20;
3. **Select certificate** - Select the required certificate. If the certificate you want to use isn't displayed, use the **Add certificate** option to add it. When done, select **Next**.
4. **Create agreement** - Choose whether you want to create a new Microsoft tenant or connect your existing cloud account.
5. **Microsoft details** - Do the following depending on the selection in the previous step:
   1. For a new cloud account, provide a new domain name and then fill out the contact form. You'll need to provide the following details:
      1. Company name.
      2. Company registration ID or tax number.
      3. Company address, including city and zip/postal code.
      4. Contact details of the person who will manage your account.
   2. For an existing cloud account, enter your existing domain name and your Microsoft account details.
6. **Special qualifications** - Select the checkbox if your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity. Otherwise, leave it clear. A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
7. **Support contacts** - Enter the contact details of your support administrator and choose your preferred support language. Select **Next**.
8. **Items** - Complete the following steps and select **Next**.
   1. Make sure to read and understand the attestation: "By clicking **Next**, I confirm that my organization is acting as an indirect partner when choosing a reseller and as a direct partner in the absence of selecting a reselle&#x72;_"._
   2. Select **Add items** to choose the items you want to order.&#x20;
   3. When the items are added, review and adjust the quantity as required.
9. **Details -** Provide reference details, like additional IDs or notes, and select **Next**.
10. **Review order** - Read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
11. **Summary** - Select **View details** to go to the order details page. Otherwise, select **Close**.
{% endstep %}
{% endstepper %}

## Next steps <a href="#next-steps" id="next-steps"></a>

When your order has been placed, we verify the order details.

If there are issues with your order, the [order details](../../../modules-and-features/marketplace/orders/#subscription-details) page will provide information about the problem and any actions you may need to take.
