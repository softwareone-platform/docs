# View credit memos associated with an invoice

When a credit memo is issued for an invoice, SoftwareOne Marketplace displays the relationship between the invoice and its associated credit memos.

{% hint style="info" %}
* Marketplace can only associate a credit memo with an invoice when a valid invoice reference is available from the source billing system. If the reference is unavailable, the association cannot be displayed in Marketplace.
* A credit memo does not change the invoice status. For example, an invoice may continue to display a status of **Paid** while also showing associated credit memos.
{% endhint %}

### Identify invoices with credit memos

The **Invoices** details page now includes a **Credit Memo** field that indicates whether an invoice has associated credit memo records. This field displays one of the following values:

<table><thead><tr><th width="255">Credit Memo Value</th><th>Meaning</th></tr></thead><tbody><tr><td>—</td><td>No credit memo is associated.</td></tr><tr><td>Credit memo number (for example, CRM-456)</td><td>One credit memo is associated.</td></tr><tr><td>Number (for example, 4)</td><td>Multiple credit memos are associated.</td></tr></tbody></table>

When the invoice is associated with more than one credit memo, the invoice overview displays the number of associated credit memos.&#x20;

To view the associated credit memos, open the invoice details page.

### View associated credit memos

To view associated credit memos:

1. Go to **Billing** > **Invoices**.
2. Select the required invoice.&#x20;
3. Review the **Credit Memo** field and associated credit memo information displayed on the invoice details page.

When associated credit memos exist, a credit memo indicator is displayed in the invoice header.

Additionally, a message is displayed under the **Invoice ID** indicating that a credit memo is associated with the invoice.

### View the original invoice from a credit memo

You can also navigate from a credit memo to its original invoice. The **Credit Memos** page includes the Marketplace invoice ID and the original invoice number.&#x20;

This allows you to easily identify the relationship between invoices and credit memos:

* Invoice > Credit Memo
* Credit Memo > Original Invoice
