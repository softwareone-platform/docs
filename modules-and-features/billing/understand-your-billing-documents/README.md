# Understand Your Billing Documents

The Marketplace Platform's automated billing process generates invoices monthly. These invoices contain subscription charges or usage data recorded in the previous calendar month.&#x20;

For many cloud-based services, such as Microsoft Azure and Adobe VIP Marketplace, the usage data can result in multiple charge lines on a single billing statement. When each charge line is printed individually on a single invoice, it's challenging to read and interpret.

To enhance clarity and help you monitor charges efficiently, the Marketplace Platform issues two types of billing documents: **Invoices** and **Statements**. These documents contain important information about your transactions.&#x20;

To learn more, continue reading or watch the following video guide:

{% embed url="https://www.youtube.com/watch?v=dmGAcCf17oE" %}
Watch our video guide about invoices and statements in recurring billing
{% endembed %}

## Billing invoices

Invoice PDFs are generated for a specific Marketplace agreement. Each invoice includes general invoice information, subscription details, and consolidated charges for all items within the subscription.&#x20;

You can view your invoice on the [Invoices](../../marketplace/billing/invoices/) page in the Marketplace Platform. To download a sample invoice, use the following link:

{% file src="../../../.gitbook/assets/sample-invoice.pdf" %}
Download a sample Marketplace invoice
{% endfile %}

### Invoice header

This Invoice Header contains general information, such as the date your invoice was created, your customer number, and the contact person's details. The header also contains your invoice number and addresses.

The following are the key fields in this section:

<table><thead><tr><th width="167">Field</th><th>Description</th></tr></thead><tbody><tr><td>PO No. (purchase order number)</td><td><p>This is the <strong>Client Additional ID</strong> that you specify for the agreement. The value comes from the <strong>Details</strong> tab on the <a href="../../marketplace/agreements/#subscription-details">agreement details page</a>. </p><ul><li>If the value you specify exceeds 20 characters, only the first 16 characters are shown on the invoice, followed by 3 dots (...).</li></ul><ul><li>If the value is blank, a dash "—" is displayed on the invoice.  </li></ul><p>If you want to edit an existing value or add a new one, you can do this through the agreement details page in the platform. For detailed instructions, see <a href="../../marketplace/agreements/edit-agreement-id.md">Update Additional Client ID</a>. </p></td></tr><tr><td>External document number</td><td><p>This is the ID of the agreement for which the invoice was issued. </p><p></p><p>Each agreement is assigned an ID automatically by the platform. These IDs can't be changed, but you can view them in the platform along with the agreement name. For more information, see <a href="../../marketplace/agreements/">Agreements</a>.</p></td></tr><tr><td>Your reference</td><td><p>This is the ID of the statement linked to the invoice. </p><p></p><p>A statement is an Excel file containing a detailed breakdown of what you are being billed for. To learn more, see <a href="./#billing-statements">Billing statements</a>. </p><p></p><p>Similar to an agreement ID, statement IDs are also assigned by the platform and can't be changed. For more information, see <a href="../../marketplace/billing/statements.md">Statements</a> and <a href="../../marketplace/billing/statements/download-statements.md">View or Download Statements</a>.</p></td></tr></tbody></table>

### Invoice line item details

The Line Item Details section contains a list of all subscriptions and items for which you are being billed. This section contains various columns, each displaying specific information, and it may span multiple pages.

The following are the key columns in this section:

<table><thead><tr><th width="137">Column</th><th>Description</th></tr></thead><tbody><tr><td>Pos </td><td><p>Displays the line number for the item being billed. </p><p>The value starts from 10 and continues by +10 for each billing item. It means if 5 items are being billed, the POS begins from 10 and ends at 50.</p></td></tr><tr><td>No.</td><td>Displays the item number from SoftwareOne's ERP system.</td></tr><tr><td>Description</td><td><p>This is the main column listing all subscriptions and items for which you are being invoiced. It contains:</p><p></p><ul><li>A link to access the statement directly in the platform.</li><li>Agreement-related information, including agreement ID and name, product details, and licensee details.</li></ul><ul><li>Subscription-related information, including subscription ID and name. You can also view the additional client ID mapped to the subscription (if there's no value, a dash is displayed), and the vendor ID.</li><li>Allocation percentage, if <a href="https://docs.platform.softwareone.com/modules-and-features/billing/split-billing">split billing</a> is enabled.</li></ul><ul><li>Total number of items within the subscription, but only if the subscription is active at the time of billing (for example, 'Qty 20 of ITM-XXXX-XXXX-XXXX / 65325070CA'). If the subscription is inactive, the item is represented as 'ITM-XXXX-XXXX-XXXX / 65325070CA' instead. </li></ul><div><figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div><div><figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div></td></tr><tr><td>Start Date - end date</td><td>Displays the duration of the charge.</td></tr><tr><td>Qty</td><td><p>Displays the quantity of items. </p><p>The value is always '1' because we consolidate all charges. For the actual item quantity, see your billing statement. </p></td></tr><tr><td>Unit price</td><td>Displays the total charge for each item in the subscription.</td></tr><tr><td>VAT %</td><td>The VAT percentage applicable to the item.</td></tr><tr><td>Total excl. VAT</td><td>The subtotal without any taxes. </td></tr><tr><td>Total incl. VAT</td><td>The total amount due with tax.</td></tr></tbody></table>

### VAT amount specification

This VAT Amount Specification section contains a breakdown of the tax. It shows how the VAT is calculated and applied to the total amount.

### Payment instructions <a href="#payment-instructions" id="payment-instructions"></a>

This section outlines the payment terms in accordance with your contract and the date when the payment is due. The section may also contain our bank account information for electronic payments.

## Billing statements

A billing statement is a detailed record of charges, and it's issued for each invoice.&#x20;

Unlike an invoice PDF, which only provides a summary of charges, a statement contains a comprehensive breakdown of all charges. To view a sample statement, use the following link:

{% file src="../../../.gitbook/assets/sample-statement.xlsx" %}
Download a sample Marketplace billing statement
{% endfile %}

A SoftwareOne Marketplace billing statement contains these tabs:

* **Summary** - Contains different objects associated with the statement, such as agreement, licensee, and orders. The page also contains links that you can use to access these objects directly in the platform.
* **Charges** - Contains a list of charges and subscriptions for the billing period. You can also view all items within the subscription, their quantities, and prices. If [split billing](../../marketplace/billing/split-billing/) has been enabled, the subscription allocation percentage and estimated license count (ELC) details are also displayed.&#x20;
* **Orders** - Contains all orders placed during the billing period and their corresponding details, such as the type of order, the date when the order was placed, and more.

## Differences between invoices and statements <a href="#key-differences-statement-vs.-invoice" id="key-differences-statement-vs.-invoice"></a>

An invoice and a statement are both billing documents, but they serve different purposes. The following table lists the key differences between these two types of documents:

<table><thead><tr><th width="198">Component</th><th width="267">Invoice</th><th width="249">Statement</th></tr></thead><tbody><tr><td>Purpose</td><td>Provides a high-level summary of the charges.</td><td>Provides a full record of the charges from the vendor.</td></tr><tr><td>Format</td><td>PDF</td><td>Excel</td></tr><tr><td>Level of detail</td><td>Contains aggregated lines, such as per item, per subscription, and so on.</td><td>Can have hundreds or thousands of lines for precise usage.</td></tr><tr><td>Use case</td><td>Used as an official billing and record-keeping document.</td><td>Used for reconciliation, in-depth audits, and analysis.</td></tr><tr><td>Quantity</td><td>Always displays the quantity as 1 because multiple lines are consolidated.</td><td>Each line shows the actual quantity of items.</td></tr></tbody></table>

{% hint style="info" %}
**Have billing-related questions?**&#x20;

See this FAQ to get answers to commonly asked questions:[ I have questions about billing](../../../help-and-support/faqs/i-have-questions-about-billing.md).
{% endhint %}
