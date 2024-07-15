# How do you handle purchase order numbers in subscription-based models?

Subscription-based models are designed to streamline licensing and renewal processes, offering a more seamless experience for managing software and service subscriptions. This model differs significantly from traditional transaction-based purchasing in several key ways.

## Subscription-based billing

Unlike transactional purchases that occur individually, subscription-based models operate regularly. You commit to a term that provides continuous access to services or software without the need to manage individual licenses manually.

## Consolidated invoicing

Invoices in a subscription-based model are consolidated, typically on a monthly or annual basis, depending on the subscription terms agreed upon.&#x20;

It means multiple purchases or renewals are grouped into single invoices, reducing the number of individual transactions.

## Purchase orders in a subscription model <a href="#handling-purchase-orders-in-the-subscription-model" id="handling-purchase-orders-in-the-subscription-model"></a>

One of the significant changes in subscription-based models involves the handling of Purchase Order (PO) numbers:

* **Non-direct linkage of PO numbers** - In traditional models, each PO number is directly linked to a specific invoice or order. However, in subscription-based models, PO numbers are not directly tied to individual invoices or subscriptions due to the consolidated nature of billing.
* **Use of PO numbers** - Although PO numbers are not linked to specific invoices, they are still crucial for internal tracking, budgeting, and financial reconciliation. PO numbers can be referenced in the consolidated invoice to maintain a connection to internal purchase processes.

## Guidance on PO numbers and invoices <a href="#client-guidance-on-po-numbers-and-invoices" id="client-guidance-on-po-numbers-and-invoices"></a>

Here’s how you can manage PO numbers and display them on invoices under subscription-based models:

### Providing PO numbers

When setting up your order, ensure that you provide your open PO number if your organization's purchasing process requires it.&#x20;

This number will be noted and used for reference in all consolidated invoices in the scope of each Agreement in the Marketplace Platform.&#x20;

You can find the example of the **Additional ID** field, which is displayed on the consolidated invoice header if provided.

<figure><img src="../../.gitbook/assets/image (452).png" alt=""><figcaption><p>Additional ID field</p></figcaption></figure>

### Displaying PO numbers on invoices

While PO numbers will not be tied to specific transactions within the invoice, they can still be displayed on each invoice as a reference point. This helps maintain traceability for financial auditing and internal tracking.&#x20;

The following is an example of the invoice header with **External Agreement ID**.

<figure><img src="../../.gitbook/assets/image (453).png" alt=""><figcaption><p>The header of an invoice (example)</p></figcaption></figure>

### Updating or changing PO numbers

If a PO number needs updating or changing during the subscription term, you can modify the **Agreement External ID**, which will then be reflected on the next invoice.

{% hint style="info" %}
This option is available for Adobe VIP Marketplace products only.
{% endhint %}

## Understanding open POs

An Open PO refers to a purchase order that remains active over a certain period and covers multiple transactions or billing cycles.&#x20;

Unlike traditional POs, which are specific to single transactions, an Open PO is designed to accommodate ongoing purchases or subscriptions under a single order number. This approach is useful in environments where regular, repeated purchases are common, such as in subscription-based billing systems.&#x20;

When setting up an agreement, you can issue an Open PO that covers the expected expense of the agreement for a defined term, such as one year. This PO should account for all foreseeable charges, including potential add-ons or tier changes.

## Conclusion <a href="#conclusion" id="conclusion"></a>

The shift to subscription-based models represents a transformation in how software and services are managed, moving from transaction-specific billing to a more streamlined, subscription-oriented approach.&#x20;

Understanding the handling of PO numbers in this new context is crucial for effective financial management and operational efficiency.

For further details or specific inquiries, contact our [support team](../getting-support.md).&#x20;
