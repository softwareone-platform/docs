# Buyers

In the Marketplace Platform, a buyer is defined as an organization that procures products or services from SoftwareOne. Buyers are recognized as legal entities within SoftwareOne's ERP system and are the recipients of invoices issued by SoftwareOne.

Account administrators can update buyer details and enable or disable buyers. However, admins cannot add new buyers to the account. Only SoftwareOne can add buyers.&#x20;

Admins can also view all buyers on the **Buyers** page, available under **Settings** in the main navigation menu.&#x20;

<figure><img src="../../../.gitbook/assets/Buyers.png" alt=""><figcaption><p>Buyers page</p></figcaption></figure>

For each buyer, you can view details such as the buyer's name and address, tax identifier, contact person, and more.&#x20;

You can also view buyer status with possible values, including:

* **Enabled** - Indicates that the buyer has been created in the system, but it hasn't been activated yet by SoftwareOne.
* **Active** - Indicates that the buyer is active, and you can select it from your list of buyers when ordering products.
* **Disabled** - Indicates that the buyer has been disabled, and you can no longer select it when buying products.
* **Mismatch** - Indicates that the buyer’s data is not in sync with our backend system. This discrepancy can occur for several reasons. [Contact support](../../../help-and-support/contact-support.md) for assistance.

You also have action links that allow you to enable, disable, or edit the buyer. These options are visible only if you have access to the Account Management module in the platform.

## Viewing buyer details

To view the details page for a buyer, select the buyer on the **Buyers** page.&#x20;

<figure><img src="../../../.gitbook/assets/BuyerDetails.png" alt=""><figcaption><p>Details page of a buyer</p></figcaption></figure>

The details page provides general information, such as the buyer's name and ID. You can also view:

* **Account** details, including the name, ID, and status.
* **SCU identifier**, which represents a unique ID for your customer card or profile within the SoftwareOne ERP system.
* **Tax number** for the buyer.

The details page also contains the following tabs:

<table><thead><tr><th width="156">Tab</th><th>Description</th></tr></thead><tbody><tr><td><strong>General</strong></td><td><p>Displays the buyer's address and the contact person's details. </p><p></p><p>Note that in the Marketplace platform, the buyer's address fields must meet certain requirements. If any address fields are empty, the SoftwareOne ERP system automatically fills them with the word '<strong>unknown'</strong>. If you notice this, <a href="../../../help-and-support/contact-support.md">contact support</a> for assistance. </p></td></tr><tr><td><strong>Sellers</strong> </td><td><p>Displays the SoftwareOne entity associated with the buyer. There's a 1:1 relationship between a buyer and seller, meaning each buyer is linked to one or more sellers.</p><p></p><p>The <strong>ERP link status</strong> is also displayed on this tab. An ERP link is a reference to the customer record in the SoftwareOne ERP system. A <strong>Blocked</strong> ERP link indicates that you cannot transact with the specified seller. In such cases, <a href="../../../help-and-support/contact-support.md">contact support</a> for assistance.</p></td></tr><tr><td><strong>Licensees</strong> </td><td>Displays the licensees associated with the buyer, along with their details. </td></tr><tr><td><strong>Details</strong> </td><td>Displays timestamps for various events and external IDs, such as Customer Discount Group (CDG) and Company Contact (CON) identifier. </td></tr><tr><td><strong>Audit trail</strong></td><td>Displays an audit trail of events. For each audit record, you can view the log details and summary. To learn more, see <a href="../audit-trail.md">Audit Trail</a>.</td></tr></tbody></table>

## Additional actions

On the details page, you can perform various actions based on the buyer's status, including:

* [Edit a buyer](edit-buyers.md)
* [Enable or disable a buyer](enable-or-disable-buyers.md)
