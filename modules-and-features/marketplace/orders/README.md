# Orders

In the Marketplace Platform, an order is an object signifying a business transaction based on an agreement.&#x20;

An order represents a request to buy a new product, change the quantity of licenses, terminate a subscription, or terminate an agreement. Therefore, different types of orders exist in the Marketplace Platform, including:

* **Purchase orders** - These orders represent an order to buy a new product or service under a new agreement.
* **Change orders** - These orders represent an order to change the subscription quantity, such as downsizing the license quantity or ordering additional licenses.
* **Terminate order** - These orders represent an order to terminate a subscription or agreement.&#x20;

## Orders interface

You can access the **Orders** page by selecting **Marketplace** > **Orders** from the main menu.

<figure><img src="../../../.gitbook/assets/image (948).png" alt=""><figcaption><p>Orders page</p></figcaption></figure>

The **Orders** page shows a complete list of your orders, including purchase, change, and termination orders. It also contains a **Buy more** option, which gives you quick access to the [Products ](https://docs.platform.softwareone.com/~/changes/5yDo0W9JFVZsyIwbYXyj/modules-and-features/marketplace/products)page for ordering new subscriptions.

For each order, you can view the following details:

* **Order** - Displays the order number and ID.
* **Type** - Displays the order type. The possible values are **Purchase**, **Change**, and **Terminate**.
* **Agreement** - Displays the agreement associated with the order.&#x20;
* **Product** - Displays the product you've ordered.
* **Licensee** - Displays the licensee associated with the order.
* **Buyer** -  Displays the buyer associated with this order.
* **Seller** - Displays the SoftwareOne entity that fulfilled the order and issued the invoice.
* **SPx** - Displays the estimated sales price of the order.
* **Created** - Displays the date when the order was created in the platform.
* **Status** - Displays the order status. To learn about the possible statuses, see [Order States](order-states.md).
* **Updated** - Displays the date when the order was updated.
* **Currency** - Displays the order currency.

### Order details page <a href="#subscription-details" id="subscription-details"></a>

The details page of an order provides detailed information about the order. You can open the details page by clicking the order on the **Orders** page.&#x20;

<details>

<summary>What can I do on this page?</summary>

From the details page, you can complete the following tasks:&#x20;

* [Submit a draft order for processing](submit-draft-orders.md)
* [Delete a draft order](delete-draft-orders.md)
* [Manage your order notes](manage-order-notes.md)
* [Change your order's status to Processing](set-an-order-to-processing.md)
* [View and download attachments](../agreements/view-and-download-attachments.md)

</details>

<figure><img src="../../../.gitbook/assets/Orders (4).png" alt=""><figcaption><p>Order details page</p></figcaption></figure>

The details page of an order contains the **Process** button that lets you [move your order from Querying to Processing](set-an-order-to-processing.md). It also contains several tabs that display the corresponding order information:

* **General** - Displays the latest information about your order.
* **Items** - Displays the items you've ordered and the pricing information for each item.
* **Parameters** - Displays the ordering and fulfillment parameters associated with the order.&#x20;
* **Entities** - Displays details of the different entities associated with the order, like the licensee, buyer, and seller.
* **Subscriptions** - Displays the subscriptions associated with the order. Subscriptions are only displayed after they have been activated. Once activated, you can view subscription details, like the term, the start and the renewal date, the estimated prices, and more.
* **Notes** - Displays the notes entered during the ordering process. Use the **Edit** option to edit the notes.
* **Attachments** - Displays the files attached to the agreement and allows you to download those files. See [View and Download Attachments](../agreements/view-and-download-attachments.md) to learn more.
* **Details** - Displays the additional IDs, including the client and vendor IDs, and the timestamps of all changes made to the order. You can update the client ID using the **Edit** option.
* **Audit trail** - Displays all events that have taken place within the order. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](../../settings/audit-trail.md).&#x20;

## Related topics

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/order-states" %}
[Order States](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/order-states)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/save-order-as-a-draft" %}
[Save Your Order as a Draft](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/save-order-as-a-draft)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/delete-draft-orders" %}
[Delete Draft Orders](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/delete-draft-orders)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/submit-draft-orders" %}
[Submit Draft Orders](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/submit-draft-orders)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/manage-order-notes" %}
[Manage Order Notes](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/manage-order-notes)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/set-an-order-to-processing" %}
[Change Your Order's Status to Processing](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/marketplace/orders/set-an-order-to-processing)
{% endcontent-ref %}
