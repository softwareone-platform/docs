---
description: Learn about buyers in the Marketplace Platform.
---

# Buyers

In the SoftwareOne Marketplace, a buyer is an organization that purchases products or services from SoftwareOne.&#x20;

Buyers are registered as legal entities within SoftwareOne's ERP system, and they are the recipients of invoices issued by SoftwareOne. All buyers are added to an account by SoftwareOne.

### Viewing and managing buyers

Account administrators can view and manage buyers from the **Buyers** page.&#x20;

When you open the page, all buyers in the account are displayed. For each buyer, you can view key details, including the buyer's name and address, tax identifier, and contact person.&#x20;

Additionally, you can view the buyer's status, including:

* **Enabled** - Indicates that the buyer has been created in the system, but it hasn't been activated yet by SoftwareOne.
* **Active** - Indicates that the buyer is active, and you can select it from your list of buyers when ordering products.
* **Disabled** - Indicates that the buyer has been disabled, and you can no longer select it when buying products.
* **Mismatch** - Indicates that the buyer’s data is not in sync with our backend system. This discrepancy can occur for several reasons. [Contact support](../../../help-and-support/contact-support.md) for assistance.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Buyers.png" alt=""><figcaption><p>The Buyers page  in the platform.</p></figcaption></figure></div>

### Viewing buyer details

On the buyer details page, you can view the extended information for your selected buyer.

To view the details page for a buyer:

1. Navigate to the **Buyers** page.
2. (Optional) Use filters to find the desired buyer.
3. Select the buyer's name to view the following information:
   * Account details, including the name, ID, and status.
   * SCU identifier, which represents a unique ID for your customer card or profile within the SoftwareOne ERP system.
   * Tax number for the buyer.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/BuyerDetails.png" alt=""><figcaption><p>The details page of a buyer.</p></figcaption></figure></div>

4. Use the following tabs to access additional related information:
   * **General** - Displays the buyer's address and the contact person's details.
   * **Sellers**  - Displays the SoftwareOne entity associated with the buyer. There's a 1:1 relationship between a buyer and seller, meaning each buyer is linked to one or more sellers. The **ERP link status** is also displayed on this tab. An **ERP link** is a reference to the customer record in the SoftwareOne ERP system.
   * **Licensees** - Displays the licensees associated with the buyer, along with their details.&#x20;
   * **Details** - Displays timestamps for various events and external IDs, such as Customer Discount Group (CDG) and Company Contact (CON) identifiers.&#x20;
   * **Audit trail** - Displays a log of events for the buyer. For more information, see [Audit Trail](../audit-trail.md).

{% hint style="warning" %}
* In the Marketplace platform, the buyer's address fields must meet certain requirements. If any address fields are empty on the **General** tab, the SoftwareOne ERP system automatically fills them with the word '**unknown'**. If you notice this, [contact support](../../../help-and-support/contact-support.md) for assistance.&#x20;
* If the status of the ERP link is **Blocked**, it indicates that you cannot transact with the specified seller. In such cases, [contact support](../../../help-and-support/contact-support.md) for assistance.
{% endhint %}

### Additional actions

You can perform various actions on the **Buyers** and **Buyers' details** pages. The actions available depend on the licensee's current status:

* [Edit a buyer](edit-buyers.md)
* [Enable or disable a buyer](enable-or-disable-buyers.md)
