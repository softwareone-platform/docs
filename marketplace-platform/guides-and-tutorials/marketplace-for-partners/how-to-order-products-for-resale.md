---
description: Order software products for reselling to your end customers.
---

# How to order products for resale

Order Microsoft products for resale from the SoftwareOne Marketplace.

When ordering products, there are two options for agreements:

* If you have an existing agreement, you can use that agreement. However, make sure the agreement is mapped to a licensee that is configured as a **resale licensee**.
* If you don't have an agreement, you can create it when placing the order. If you choose to create a new agreement, you must select an existing licensee that is configured as a **resale licensee**.

For a quick walkthrough of the wizard layout, see [How does the Marketplace purchase wizard work?](../../../help-and-support/faqs/buy-products-and-services.md).

### Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* A resale licensee in the active state, or permission to [configure a licensee for resale](how-to-configure-licensees-for-resale.md) if you don't want to use an existing one. Licensee selection is required when setting up a new agreement.
* Company details of your client, including the company name, registration ID, and address. These details are required for creating a new Microsoft tenant.
* The contact details of your client managing the Microsoft account.

### Ordering software products for resale

{% stepper %}
{% step %}
{% include "../../../.gitbook/includes/purchase-wizard-1.md" %}

To start the process:

1. Go to **Catalog** > **Products**.
2. From the list of products, select the desired Microsoft 365 product, for example, **Microsoft 365 Business, Enterprise & Apps**.
3. On the **product details** page, review the information, then select **Buy now**.
{% endstep %}

{% step %}
{% include "../../../.gitbook/includes/purchase-wizard-2.md" %}

{% include "../../../.gitbook/includes/in-the-purchase-wizard-com....md" %}

1. **Select agreements** - Select **Create agreement** to start creating your new agreement. If you want to reuse an agreement, check [View agreements](../../../modules-and-features/marketplace/agreements/view-agreements.md) first.
2. **Select licensee** - Choose an existing licensee from the list. Ensure that the value in the **Resale** column is **Yes**, then select **Next**.
3. **Select certificate** - Select a certificate. If the certificate you want to use isn't displayed, use the **Add certificate** option to add it. Use [View certificates](../../../modules-and-features/program/certificates/view-certificates.md) to confirm the certificate is available, or check [Certificate status](../../../modules-and-features/program/certificates/certificate-states.md) if it is still processing. When done, select **Next**.
4. **Create agreement** - Choose whether you want to create a new Microsoft tenant or connect an existing cloud account.
5. **Microsoft details** - Do the following depending on the selection in the previous step:
   * For a new cloud account, provide a new domain name and then fill out the contact form. You'll need to provide the following details:
     1. Company name.
     2. Company registration ID or tax number.
     3. Company address, including city and zip/postal code.
     4. Contact details of the person managing your account.
   * For an existing cloud account, enter your existing domain name and your Microsoft account details.
6. **Special qualifications** - Select the checkbox if your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity. Otherwise, leave it clear. A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
7. **Support contacts** - Enter the contact details of your support administrator and choose your preferred support language. Select **Next**.
8. **Items** - Complete the following steps and select **Next**.
   1. Read and understand the attestation: "_By clicking **Next**, I confirm that my organization is acting as an indirect partner when choosing a reseller and as a direct partner in the absence of selecting a reseller"._
   2. Select **Add items** to choose the items you want to order.
   3. Review and adjust the item quantity.
9. **Details -** Provide reference details, like additional IDs or notes, and select **Next**.
10. **Review order** - Read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
11. **Summary** - Select **View details** to open the order details page. Otherwise, select **Close**.
{% endstep %}
{% endstepper %}

### Next steps <a href="#next-steps" id="next-steps"></a>

When your order has been placed, we verify the order details.

If there are issues with your order, the **General** tab on the[ order details page](../../../modules-and-features/marketplace/orders/#order-details) provides information about the problem and the actions you must take before your order can be processed.

Track the order in [View orders](../../../modules-and-features/marketplace/orders/view-orders.md), or open the [order details page](../../../modules-and-features/marketplace/orders/view-orders.md#order-details) to review issues and required actions.
