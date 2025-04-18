# Orders

In the Marketplace Platform, an order represents a request to buy a new product, change the number of licenses, terminate a subscription, or terminate an agreement.&#x20;

There are different types of orders in the Marketplace Platform:

* **Purchase orders** - An order to buy a new product or service by establishing a new agreement.
* **Change orders** - An order to change the quantity, such as downsizing the quantity of licenses or ordering additional licenses.
* **Terminate order** - An order to terminate an active subscription or an agreement.&#x20;
* **Configuration order** - An order to enable or disable the auto-renewal of a subscription.

You can view and manage your orders from the **Orders** page in the platform.

<figure><img src="../../../.gitbook/assets/orders_page.png" alt=""><figcaption><p>Orders page</p></figcaption></figure>

For each order, the orders page displays the following details:

* **Order** - Displays the order number and ID.
* **Type** - Displays the type of order, such as **Purchase**, **Change**, **Terminate,** or **Configuration**.
* **Agreement** - Displays the agreement under which that order has been placed.&#x20;
* **Product** - Displays the product that was ordered.
* **Licensee** - Displays the licensee for the order.
* **Buyer** -  Displays the buyer associated with the order.
* **Seller** - Displays the SoftwareOne entity that fulfilled the order and issued the invoice.
* **SPx** - Displays the estimated sales price of the order.
* **Created** - Displays the date when the order was created.
* **Status** - Displays the order status. To learn about the possible statuses, see [Order States](order-states.md).
* **Updated** - Displays the date when the order was updated.
* **Currency** - Displays the order's currency.

## Viewing order details <a href="#subscription-details" id="subscription-details"></a>

To access an order's details page, select the link in the **Order** column on the **Orders** page.

<figure><img src="../../../.gitbook/assets/order_details_page.png" alt=""><figcaption><p>Order details page</p></figcaption></figure>

The details page contains the following tabs:

* **General** - Displays the latest information about your order.
* **Items** - Displays the items you've ordered and the pricing information for each item.
* **Parameters** - Displays the ordering and fulfillment parameters associated with the order.&#x20;
* **Entities** - Displays details of the different entities associated with the order, like the licensee, buyer, and seller.
* **Subscriptions** - Displays the subscriptions associated with the order. Subscriptions are only displayed after they are activated. When activated, you can view subscription details, like the term, the start and the renewal date, the estimated prices, and more.
* **Notes** - Displays the notes entered during the ordering process. Use the **Edit** option to edit the notes.
* **Attachments** - Displays the files attached to the agreement and allows you to download those files. See [View and Download Attachments](../agreements/view-and-download-attachments.md) to learn more.
* **Certificates** - Displays the certificates that were used when the order was placed.&#x20;
* **Details** - Displays the additional IDs, including the client and vendor IDs, and the timestamps of all changes made to the order. You can update the client ID using the **Edit** option.
* **Audit trail** - Displays all events that have taken place within the order. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](../../settings/audit-trail.md).&#x20;

## Managing orders

From the order details page, you can complete the following tasks:&#x20;

* [Delete a draft order](delete-draft-orders.md)
* [Manage the notes for your order](manage-order-notes.md)
* [Change your order's status to Processing](set-an-order-to-processing.md)
* [View and download attachments](../agreements/view-and-download-attachments.md)

## Related topics

{% content-ref url="order-states.md" %}
[order-states.md](order-states.md)
{% endcontent-ref %}

{% content-ref url="save-order-as-a-draft.md" %}
[save-order-as-a-draft.md](save-order-as-a-draft.md)
{% endcontent-ref %}

{% content-ref url="delete-draft-orders.md" %}
[delete-draft-orders.md](delete-draft-orders.md)
{% endcontent-ref %}

{% content-ref url="submit-draft-orders.md" %}
[submit-draft-orders.md](submit-draft-orders.md)
{% endcontent-ref %}

{% content-ref url="manage-order-notes.md" %}
[manage-order-notes.md](manage-order-notes.md)
{% endcontent-ref %}

{% content-ref url="set-an-order-to-processing.md" %}
[set-an-order-to-processing.md](set-an-order-to-processing.md)
{% endcontent-ref %}
