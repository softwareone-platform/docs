# Invoices

An invoice is a billing document that you receive at the end of your billing period.&#x20;

Invoices contain a summary of charges and other details associated with your account. Invoice PDFs also include subscription details and the consolidated charges for all items within the subscription. See [Understand Your Billing Documents](../understand-your-billing-documents.md) to learn more.

You can view your invoices on the **Invoices** page in the platform.&#x20;

<figure><img src="../../../../.gitbook/assets/invoices_page.png" alt=""><figcaption><p>Invoices page in the platform</p></figcaption></figure>

For each invoice, you can view the following details:

* **ID** - Displays the unique ID of the invoice. Select the **ID** to display the invoice details page.
* **Type** - Displays the type of invoice:&#x20;
  * **Debit** - A debit invoice is an invoice that shows a summary of charges and the total payable amount.
  * **Credit** - A credit invoice is a memo that is generated for negative charges, such as refunds and returns. Credit memos have a negative total but can still be tied to a statement.
* **Buyer** - Displays the buyer linked to the agreement.
* **Vendor** - Displays the name and ID of the vendor that made the charge. &#x20;
* **Product** - Displays the name and ID of the product in the Marketplace.
* **Agreement** - Displays the name and ID of the agreement associated with the subscriptions that are getting billed.
* **Seller** - Displays the name and ID of the SoftwareOne entity that issued the invoice.
* **SP** - Represents the total amount of the invoice. <mark style="color:red;">**Does SP mean sales price here?**</mark>
* **Status** - Displays the status of the invoice, such as **Paid**, **Overdue**, or **Generated**. <mark style="color:red;">**Are there more states?**</mark>
  * **Paid** - The invoice has been paid in full. No further action is required.
  * **Overdue** - The invoice is past due. Invoices in this state require immediate action to prevent service disruptions. Note that overdue invoices may attract penalties, interest, or both, depending on your terms and conditions.
  * **Generated** - The invoice has been generated and issued, but it has not been settled yet.
* **Created** - Displays the date when the invoice was created.&#x20;

## Viewing invoice details <a href="#subscription-details" id="subscription-details"></a>

To view the details page of an invoice, select the link for the invoice in the **Invoices** column.&#x20;

The details page displays various properties associated with the invoice, such as agreement details, buyer details, and vendor details. You can also view the currency you are been invoiced in and the invoice amount.

<figure><img src="../../../../.gitbook/assets/invoice_details_page.png" alt=""><figcaption><p>Detials page of an invoice</p></figcaption></figure>

The details page also contains the following tabs:&#x20;

* **Records** - Displays various details associated with the invoice, such as the billing cycle, the number of licenses, and charges.
* **Attachments** - Displays the invoice PDF and allows you to download it.&#x20;
* **Details** - Displays the reference information for the invoice, like the additional IDs and timestamps.
* **Audit trail** - Displays an audit trail of all events for the invoice. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](../../../settings/audit-trail.md).
