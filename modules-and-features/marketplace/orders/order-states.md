# Order States

An order can have several states from the time it's created until its completion.&#x20;

The following diagram shows how an order's state can change during its lifecycle:

<figure><img src="../../../.gitbook/assets/state_diagram_orders.png" alt=""><figcaption><p>Order state transition</p></figcaption></figure>

<table><thead><tr><th width="140">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The platform has created the order as a draft. This status applies to orders created by the system for validation purposes. It doesn't apply to orders saved for later during the ordering process.</td></tr><tr><td><strong>Quoted</strong></td><td>The order was intentionally saved for later using the <strong>Save Order</strong> option, available when creating purchase or change orders.</td></tr><tr><td><strong>Processing</strong></td><td>The order has been created, and it's currently awaiting processing by the vendor.</td></tr><tr><td><strong>Querying</strong></td><td>The ordering parameters have been updated by the vendor. The order requires an action to be taken by the client.</td></tr><tr><td><strong>Completed</strong></td><td>The order has been processed by the vendor.</td></tr><tr><td><strong>Failed</strong></td><td>The order has been marked as failed by the vendor or SoftwareOne. The failure reason is displayed on the order details page.</td></tr><tr><td><strong>Deleted</strong></td><td>The order has been deleted. This status applies to orders that have been deleted intentionally, as well as those that are removed by the platform. See <a href="../../../help-and-support/faqs/my-draft-or-quoted-order-has-been-deleted.md">My draft or quoted order has been deleted</a> to learn more.</td></tr></tbody></table>
