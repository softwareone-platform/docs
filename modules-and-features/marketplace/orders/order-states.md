---
description: Learn about the different states of an order.
---

# Order states

An order represents a transaction that starts, changes, or ends a service in Marketplace.

An order can be in one of these states: **Draft**, **Deleted**, **Quoted**, **Processing**, **Querying**, **Scheduled**, **Cancelling**, **Cancelled**, **Complete**, or **Failed**. The following diagram shows the transitions between these states:

<figure><img src="../../../.gitbook/assets/state-machine-order.png" alt=""><figcaption><p>The state transition diagram of an order.</p></figcaption></figure>

The following table describes the different states:

<table data-search="false"><thead><tr><th width="163">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The order is a draft. This status applies to orders created by the platform for validation purposes. It doesn't apply to orders saved for later during the ordering process.</td></tr><tr><td><strong>Deleted</strong></td><td>The order was deleted. This status applies to orders that are deleted intentionally and those removed by the platform. For more details, see <a href="../../../help-and-support/faqs/my-draft-or-quoted-order-has-been-deleted.md">My draft or quoted order has been deleted</a>.</td></tr><tr><td><strong>Quoted</strong></td><td>The order has been saved for later using the <strong>Save Order</strong> option during order creation.</td></tr><tr><td><strong>Processing</strong></td><td>The order is created, and it's currently awaiting processing by the vendor.</td></tr><tr><td><strong>Querying</strong></td><td>The ordering parameters are updated by the vendor. The order requires an action to be taken by the client.</td></tr><tr><td><strong>Scheduled</strong></td><td>The renewal order has been submitted, and the changes are due to take effect on the renewal date.</td></tr><tr><td><strong>Cancelling</strong></td><td>A cancellation request has been initiated for a scheduled renewal order.</td></tr><tr><td><strong>Cancelled</strong></td><td>The scheduled renewal order has been cancelled. The agreement and subscriptions remain unchanged.</td></tr><tr><td><strong>Complete</strong></td><td>The vendor has processed the order.</td></tr><tr><td><strong>Failed</strong></td><td>The order could not be processed. The reason is displayed on the order details page.</td></tr></tbody></table>
