# Understand Your Billing Documents

Your billing documents, like an invoice or statement, contain important information about your transactions.

To help you understand these documents better, we've created the following video. It breaks down the key sections within your invoices and statements and highlights important aspects to be aware of when interpreting the charges.

{% embed url="https://www.youtube.com/watch?v=dmGAcCf17oE" %}
Video: Invoice and Statement Formats in Recurring Billing
{% endembed %}

## Invoice header

This section contains general invoice information, like the date when the invoice was created, your customer number, contact person details, and more. Your invoice number and address details are also displayed in this section.

<figure><img src="../../../.gitbook/assets/invoice_header.png" alt=""><figcaption><p>Invoice header</p></figcaption></figure>

The following table lists the key fields in the invoice header:

<table><thead><tr><th width="228">Field</th><th>Description</th></tr></thead><tbody><tr><td>PO number</td><td><p>Displays a value from the <strong>Additional ID</strong> field, available on the <strong>Details</strong> tab within the <a href="../agreements/#subscription-details">agreement details page</a>. </p><p></p><ul><li>If the value exceeds 20 characters, only the first 16 characters are shown on the invoice, followed by 3 dots (...).</li><li>If the field is empty, the <strong>PO No.</strong> is displayed as  "<strong>—</strong>". To add a value, navigate to the <strong>Details</strong> tab on the agreement details page, select <strong>Edit</strong>, and enter the value under <strong>Additional IDs</strong>. </li></ul></td></tr><tr><td>External document number</td><td>Displays the ID of the agreement for which the invoice has been generated.</td></tr><tr><td>Your reference</td><td>Displays the ID of the statement associated with the invoice.</td></tr></tbody></table>

## Invoice details

This section displays all subscriptions and items for which you are being invoiced. Note that this section may be more than one page, depending on the data.&#x20;

<figure><img src="../../../.gitbook/assets/invoice_details.png" alt=""><figcaption><p>Invoice details section</p></figcaption></figure>

The following table lists the key fields in this section:

<table><thead><tr><th width="202">Column</th><th>Description</th></tr></thead><tbody><tr><td>Description</td><td><p>Includes a header that displays identifiers such as account ID, agreement ID, and more. You can also see all subscriptions linked to the agreement and the items within each subscription. </p><p></p><p>If <a href="split-billing/">split billing</a> has been enabled, the configured allocation percentage is also displayed. </p></td></tr><tr><td>Quantity</td><td>Displays the quantity of items. The value is always '1' because we consolidate all charges. See your <a href="./#whats-a-statement">Marketplace billing statement</a> for details on the actual item quantity.</td></tr><tr><td>Unit price</td><td>Displays the total charges for each item within the subscription.</td></tr></tbody></table>

## Statements <a href="#whats-a-statement" id="whats-a-statement"></a>

A billing statement provides a detailed view of your invoice data. Statements are generated as Excel files, and they contain the following tabs:&#x20;

* **Summary** - Contains different objects associated with the statement, such as agreement, licensee, and orders. The page also contains links that you can use to access these objects directly in the platform.
* **Charges** - Contains a list of charges and subscriptions for the billing period. You can also view all items within the subscription, their quantities, and prices. If [split billing](split-billing/) has been enabled, the subscription allocation percentage and estimated license count (ELC) details are also displayed.&#x20;
* **Orders** - Contains all orders placed during the billing period and their corresponding details, such as the type of order, the date when the order was placed, and more.

You can download a sample statement from the [Billing ](./)page.

## Frequently asked questions (FAQs) <a href="#invoice-faq" id="invoice-faq"></a>

### How do I display a purchase order number on the invoice?&#x20;

You can include a purchase order number by entering it in the **Additional ID** field, located on the **Details** tab within the agreement details page. For more information, see [How can I enter a purchase order number?](../../../help-and-support/faqs/how-do-you-handle-purchase-order-numbers-in-subscription-based-models.md#client-guidance-on-po-numbers-and-invoices) and [Update Additional Client ID](../agreements/edit-agreement-id.md).

### Can I view or download my statements?

Yes, you can view or download your billing statements from the **Attachments** tab on the agreement details page. For more information, see [Viewing and downloading attachments](../agreements/view-and-download-attachments.md#viewing-and-downloading-attachments).

### Why are all the subscription invoice lines marked as 'Qty 1'?

Vendors generate hundreds or thousands of charges during a billing period, and all charges can't be listed individually on the invoice PDF.&#x20;

To avoid clutter, we consolidate all charges at the item level and display the quantity as '1' on the invoice. You can view the quantity data and full set of charges in your [billing statement](./#whats-a-statement).
