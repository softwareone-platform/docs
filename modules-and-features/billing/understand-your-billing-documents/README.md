---
description: Learn how to read and interpret your Marketplace invoices and statements.
---

# Understand Your Billing Documents

For many cloud-based services, such as Microsoft Azure and Adobe VIP Marketplace, usage-based billing can result in multiple charge lines. When these charges are listed individually on a single invoice, the information can be difficult to read and interpret.&#x20;

To simplify your billing experience, the Marketplace Platform provides the following documents:&#x20;

* **Invoice** - An invoice is a PDF document that contains subscription charges and usage recorded during the previous calendar month. Invoices are issued monthly based on a specific Marketplace agreement.
* **Statement** - A statement is an Excel file containing a detailed breakdown of charges on an invoice, including individual charge lines and usage details. Statements are also issued monthly.

To learn about these documents, continue reading or watch the video guide:

{% embed url="https://www.youtube.com/watch?v=dmGAcCf17oE" %}
Watch this video guide explaining invoices and statements in recurring billing.
{% endembed %}

### Billing invoices

An invoice PDF contains general invoice information, subscription details, and charges for the items within the subscription. You can view your invoices on the [Invoices](../../marketplace/billing/invoices/) page in the platform.

#### Invoice types

We provide two types of invoices:

* **Compact invoice** - A compact invoice is a summarized invoice issued for statements containing a large number of charges (typically 42 or more). In a compact invoice, all charges for a product or service are grouped into summarized invoice lines, and quantities are shown as `1` to represent the aggregate charge for each item.&#x20;
* **Detailed invoice** - A detailed invoice is issued for statements containing a limited number of charges (typically 41 or fewer). This type of invoice lists each charge on a separate line, allowing you to see exactly what you are being billed for, line by line. This means you don't need to refer to another statement for transaction details.

The invoice type is indicated in the **Description** column of your invoice PDF. For more details, see [Invoice line item details](./#invoice-line-item-details).

#### Invoice header

This section contains general information, such as the invoice creation date, your customer number, and contact details. It also includes your invoice number and addresses.

The following are key fields in this section:

<table><thead><tr><th width="167">Field</th><th>Description</th></tr></thead><tbody><tr><td>PO No. (purchase order number)</td><td><p>This is the <strong>Client Additional ID</strong> that you specify for the agreement. The value comes from the <strong>Details</strong> tab on the <a href="../../marketplace/agreements/#subscription-details">agreement details page</a>.</p><ul><li>If the value you specify exceeds 20 characters, only the first 16 characters are shown on the invoice, followed by 3 dots (<code>...</code>).</li><li>If the value is blank, a dash (<code>—</code>) is displayed on the invoice.</li></ul><p>To edit an existing value or add a new one, use the agreement details page. For details, see <a href="../../marketplace/agreements/edit-agreement-id.md">Update Additional Client ID</a>.</p></td></tr><tr><td>External document number</td><td><p>This is the ID of the agreement for which the invoice was issued.</p><p>Each agreement is assigned an ID automatically by the platform. These IDs can't be changed, but you can view them in the platform along with the agreement name. </p></td></tr><tr><td>Your reference</td><td><p>This is the ID of the statement linked to the invoice.</p><p>Similar to an agreement ID, statement IDs are also assigned by the platform and can't be changed. </p></td></tr></tbody></table>

#### Invoice line item details

This section lists all subscriptions and items for which you are being billed. It contains multiple columns and may span multiple pages.

The following are key columns in this section:

<table><thead><tr><th width="137">Column</th><th>Description</th></tr></thead><tbody><tr><td>Pos</td><td><p>Displays the line number for the item being billed.</p><p>The value starts from 10 and continues by +10 for each billing item. It means if 5 items are being billed, the POS begins from 10 and ends at 50.</p></td></tr><tr><td>No.</td><td>Displays the item number from SoftwareOne's ERP system.</td></tr><tr><td>Description</td><td><p>This is the main column listing subscriptions and items included on the invoice. It includes:</p><ul><li>The <a href="./#invoice-types">invoice type</a> and a secure URL to download the associated statement using invoice and statement IDs. For more details, see <a href="../../marketplace/billing/statements/download-statements.md">Download Statements</a>. </li><li>Agreement information, including agreement ID and name, product details, and licensee details.</li><li>Subscription information (subscription ID and name). You can also view the additional client ID mapped to the subscription (if there's no value, a dash is displayed) and the vendor ID.</li><li>Allocation percentage, if <a href="../../marketplace/billing/split-billing/">split billing</a> is enabled.</li><li>Total number of items within the subscription, but only if the subscription is active at the time of billing (for example, 'Qty 20 of ITM-XXXX-XXXX-XXXX / 65325070CA'). If the subscription is inactive, the item is shown as 'ITM-XXXX-XXXX-XXXX / 65325070CA' instead.</li></ul><p><img src="../../../.gitbook/assets/image (7).png" alt="" data-size="original"></p><p><img src="../../../.gitbook/assets/image (9).png" alt="" data-size="original"></p></td></tr><tr><td>Start date - end date</td><td>Displays the duration of the charge.</td></tr><tr><td>Qty</td><td><p>Displays the item quantity. </p><p>On <a href="./#billing-invoices">compact invoices</a>, this value is shown as <code>1</code> because charges are consolidated. For the actual item quantities, see your billing statement.</p></td></tr><tr><td>Unit price</td><td>Displays the unit price used to calculate the line amount.</td></tr><tr><td>VAT %</td><td>The VAT percentage applicable to the item.</td></tr><tr><td>Total excl. VAT</td><td>The subtotal without taxes.</td></tr><tr><td>Total incl. VAT</td><td>The total amount due including VAT.</td></tr></tbody></table>

#### VAT amount specification

This section contains a breakdown of taxes. It shows how VAT is calculated and applied to the total amount.

#### Payment instructions <a href="#payment-instructions" id="payment-instructions"></a>

This section outlines the payment terms in accordance with your contract and the date when the payment is due. It may also contain bank account information for electronic payments.

### Billing statements

A statement is a detailed record of charges for each invoice.

Unlike invoice PDFs (which summarize charges), statements provide a comprehensive breakdown of all charges. Statements are issued as Excel (`.xlsx`) files and typically contain the following tabs:

* **Summary** - Contains objects associated with the statement (for example, agreement, licensee, and orders) with links to open them in the platform.
* **Charges** - Contains charges and subscriptions for the billing period. You can also see items within subscriptions, their quantities, and prices. If [split billing](../../marketplace/billing/split-billing/) is enabled, allocation percentage and estimated license count (ELC) details are also displayed.
* **Orders** - Contains all orders placed during the billing period, including order type, order date, and related details.

You can download your statements from the **Statements** page in the platform or use the [Billing Statement Download](https://mystatements.platform.softwareone.com/) page if you cannot access your account. For more details, see [Download Statements](../../marketplace/billing/statements/download-statements.md).
