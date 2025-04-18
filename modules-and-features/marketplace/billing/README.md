# Billing

Marketplace Platform's automated billing process issues documents based on subscription charges or usage data recorded in the previous calendar month.&#x20;

For many cloud-based services, such as Microsoft Azure and Adobe VIP Marketplace, the usage data can result in multiple charge lines on a single billing statement. When each charge line is printed individually on a single invoice, it can be challenging to read and interpret.

To enhance clarity and help you monitor charges more efficiently, the Marketplace Platform issues two types of billing documents: Invoices and Statements.

## What is an invoice? <a href="#whats-an-invoice" id="whats-an-invoice"></a>

An invoice is a billing document you receive for your purchases. Invoices are issued as PDFs in the context of specific agreements.&#x20;

They contain a summary of charges and details like your customer information, payment terms, and so on. Invoice PDFs also include subscription details and the consolidated charges for all items within the subscription. See [Understand Your Billing Documents](understand-your-billing-documents.md) for guidance on understanding the different components of an invoice.

To download a sample invoice, use the following link:

{% file src="../../../.gitbook/assets/sample_invoice.pdf" %}
Sample: Marketplace Billing Invoice
{% endfile %}

## What is a statement? <a href="#whats-a-statement" id="whats-a-statement"></a>

A billing statement is a detailed record of charges, and it is issued for each invoice. Unlike an invoice PDF, which only provides a summary of charges, a statement contains a comprehensive breakdown of all charges.&#x20;

Statements are generated as Excel files, and they contain the data for your charges and orders on separate tabs. See [Understand Your Billing Documents](understand-your-billing-documents.md) to learn more about statements.

You can download your billing statements from the **Attachments** tab on the agreement details page. See [Viewing and Downloading Attachments](../agreements/view-and-download-attachments.md) for instructions.

To download a sample statement, use the following link:

{% file src="../../../.gitbook/assets/sample_statement.xlsx" %}
Sample: Marketplace Billing Statement
{% endfile %}

## Differences between invoices and statements <a href="#key-differences-statement-vs.-invoice" id="key-differences-statement-vs.-invoice"></a>

An invoice and a statement are both billing documents, but they serve different purposes. The following table lists the key differences between these two types of documents:

<table><thead><tr><th width="249">Aspect </th><th>Invoice</th><th width="249">Statement</th></tr></thead><tbody><tr><td>Purpose</td><td>Provides a high-level summary of the charges.</td><td>Provides a full record of the charges from the vendor.</td></tr><tr><td>Format</td><td>PDF</td><td>Excel</td></tr><tr><td>Level of detail</td><td>Contains aggregated lines, such as per item, per subscription, and so on.</td><td>Can have hundreds or thousands of lines for precise usage.</td></tr><tr><td>Use case</td><td>Used as an official billing and record-keeping document.</td><td>Used for reconciliation, in-depth audits, and analysis.</td></tr><tr><td>Quantity</td><td>Always displays the quantity as 1 because multiple lines are consolidated.</td><td>Each line shows the actual quantity of items.</td></tr></tbody></table>

## Related topics

{% content-ref url="understand-your-billing-documents.md" %}
[understand-your-billing-documents.md](understand-your-billing-documents.md)
{% endcontent-ref %}

{% content-ref url="invoices/downloading-invoices.md" %}
[downloading-invoices.md](invoices/downloading-invoices.md)
{% endcontent-ref %}

{% content-ref url="statements/download-statements.md" %}
[download-statements.md](statements/download-statements.md)
{% endcontent-ref %}
