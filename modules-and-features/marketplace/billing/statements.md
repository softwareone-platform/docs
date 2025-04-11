# Statements

A statement is a billing document you receive at the end of your billing period along with your invoice PDF.

Statements are available in XLSX format and contain a detailed view of your invoice data, including individual charges and subscriptions for the billing period. See [Understand Your Billing Documents](understand-your-billing-documents.md) for guidance on understanding the different components of a statement.

In the Marketplace Platform, you can use the **Statements** page to:

* Filter your statements.
* Check your statement's status to determine if has been generated.
* View a detailed list of all charges throughout the invoice period.
* Identify the agreement or invoice associated with the statement.

## Statements interface

You can access the **Statements** page by selecting **Billing** > **Statements** from the main menu.

<figure><img src="../../../.gitbook/assets/statements.png" alt=""><figcaption><p>Statements page</p></figcaption></figure>

The **Statements** page displays all statements that have been created for your account. For each statement, you can view the following details:

* **ID** - Displays the unique ID of the statement. Click the **ID** to display the statement details page.
* **Type** - Displays the type of statement:&#x20;
  * **Debit** - <mark style="color:red;">**Description required**</mark>
  * **Credit** - <mark style="color:red;">**Description required**</mark>
* **Buyer** - Displays the buyer linked to the statement.
* **Vendor** - Displays the name and ID of the vendor that made the charge. &#x20;
* **Product** - Displays the name and ID of the product in the Marketplace.
* **Agreement** - Displays the name and ID of the agreement associated with the statement.&#x20;
* **Seller** - Displays the name and ID of the SoftwareOne entity that issued the statement.
* **Created** - Displays the date when the statement was created.&#x20;
* **SP** - Displays the total amount of the associated invoice.
* **Status** - Indicates if the statement has been generated or is pending.&#x20;

## Statement details page <a href="#subscription-details" id="subscription-details"></a>

The details page of a statement displays various properties associated with the statement, such as statement ID, agreement details, buyer and seller details, and more.&#x20;

Selecting a property in the header opens its details page. For instance, selecting the invoice ID displays the invoice details page.

<figure><img src="../../../.gitbook/assets/statement_details_page.png" alt=""><figcaption><p>Details page of a statement</p></figcaption></figure>

The details page also contains the following tabs:&#x20;

* **Charges** - Displays a list of charges and subscriptions for the billing period. You can also view all items within the subscription, the quantity of the line items, and prices.
* **Details** - Displays the reference information, like the additional IDs and timestamps.
* **Audit trail** - Displays an audit trail of events. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](../../settings/audit-trail.md).
