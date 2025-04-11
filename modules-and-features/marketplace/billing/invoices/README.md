# Invoices

An invoice is a billing document that you receive at the end of your billing period.&#x20;

Invoices contain a summary of charges and other details associated with your account. Invoice PDFs also include subscription details and the consolidated charges for all items within the subscription. See [Understand Your Billing Documents](../understand-your-billing-documents.md) for guidance on understanding the different components of an invoice.

In the Marketplace Platform, you can use invoices to see what you are being billed for and how it relates to your usage and agreements. You can use the **Invoices** page to:

* Filter your invoices.
* View detailed invoice data.
* Download a PDF of the invoice.
* Check your invoice's status to determine if has been generated, paid, or overdue.&#x20;
* Identify the agreement or statement associated with the invoice.

## Invoices interface

You can access the **Invoices** page by selecting **Billing** > **Invoices** from the main menu.

<figure><img src="../../../../.gitbook/assets/invoices_page.png" alt=""><figcaption><p>Invoices page in the platform</p></figcaption></figure>

The **Invoices** page displays all invoices that have been created for your account. For each invoice, you can view the following details:

* **ID** - Displays the unique ID of the invoice. Click the **ID** to display the invoice details page.
* **Type** - Displays the type of invoice:&#x20;
  * **Debit** - A debit invoice is an invoice that shows a summary of charges and the total payable amount.
  * **Credit** - A credit invoice is a memo that is generated for negative charges, such as refunds and returns. Credit memos have a negative total but can still be tied to a statement.
* **Buyer** - Displays the buyer linked to the agreement.
* **Vendor** - Displays the name and ID of the vendor that made the charge. &#x20;
* **Product** - Displays the name and ID of the product in the Marketplace.
* **Agreement** - Displays the name and ID of the agreement associated with the subscriptions that are getting billed.
* **Seller** - Displays the name and ID of the SoftwareOne entity that issued the invoice.
* **Created** - Displays the date when the invoice was created.&#x20;
* **SP** - Displays the total amount of the invoice.
* **Status** - Displays the status of the invoice, such as **Paid**, **Overdue**, or **Generated**.
  * **Paid** - The invoice has been paid in full. No further action is required.
  * **Overdue** - The invoice is past due. Invoices in this state require immediate action to prevent service disruptions. Note that overdue invoices may attract penalties, interest, or both, depending on your terms and conditions.
  * **Generated** - The invoice has been generated and issued, but it has not been settled yet.

## Invoice details page <a href="#subscription-details" id="subscription-details"></a>

The details page of an invoice displays various properties associated with the invoice, such as agreement details, buyer details, and vendor details. You can also view the currency you are been invoiced in and the invoice amount.

Selecting a property in the header opens its details page. For instance, selecting the statement ID opens the statement details page, where you can view a detailed list of charges for the invoice.&#x20;

<figure><img src="../../../../.gitbook/assets/invoice_details_page.png" alt=""><figcaption><p>Detials page of an invoice</p></figcaption></figure>

The details page also contains the following tabs:&#x20;

* **Records** - Displays various details associated with the invoice, such as the billing cycle, the number of licenses, and charges.
* **Attachments** - Displays the invoice PDF and allows you to download it.&#x20;
* **Details** - Displays the reference information for the invoice, like the additional IDs and timestamps.
* **Audit trail** - Displays an audit trail of all events for the invoice. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](../../../settings/audit-trail.md).
