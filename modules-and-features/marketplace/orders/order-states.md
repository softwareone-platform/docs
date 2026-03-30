---
description: Learn about the different states of an order.
---

# Order status

An order can currently exist in these states: **Draft**, **Quoted**, **Provisioning**, **Querying**, **Completed**, **Failed**, or **Deleted**. The following diagram shows the transitions between these states:

<figure><img src="../../../.gitbook/assets/state_diagram_orders.png" alt=""><figcaption><p>The state transition diagram of an order.</p></figcaption></figure>

The following table provides a description of the different statuses:

<table><thead><tr><th width="140">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The platform has created the order as a draft. This status applies to orders created by the system for validation purposes. It doesn't apply to orders saved for later during the ordering process.</td></tr><tr><td><strong>Quoted</strong></td><td>The order has been saved for later using the <strong>Save Order</strong> option during creation.</td></tr><tr><td><strong>Processing</strong></td><td>The order is created, and it's currently awaiting processing by the vendor.</td></tr><tr><td><strong>Querying</strong></td><td>The ordering parameters are updated by the vendor. The order requires an action to be taken by the client.</td></tr><tr><td><strong>Completed</strong></td><td>The order is processed by the vendor.</td></tr><tr><td><strong>Failed</strong></td><td>The order cannot be processed by the vendor or SoftwareOne. The failure reason is displayed on the order details page.</td></tr><tr><td><strong>Deleted</strong></td><td>The order is deleted. This status applies to orders that are deleted intentionally and those removed by the platform. For more details, see <a href="../../../help-and-support/faqs/my-draft-or-quoted-order-has-been-deleted.md">My draft or quoted order has been deleted</a>.</td></tr></tbody></table>
