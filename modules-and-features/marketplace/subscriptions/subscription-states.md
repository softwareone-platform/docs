---
description: Learn about the different states of a subscription.
---

# Subscription states

A subscription refers to the ongoing service provision under the terms and conditions of an agreement.

A subscription can be in one of these states: **Active**, **Updating**, **Suspending**, **Suspended**, **Resuming**, **Terminating**, **Terminated**, or **Expired**. The following diagram shows the transitions between these states:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/state machine-subscription.png" alt=""><figcaption><p>The state transition diagram of a subscription.</p></figcaption></figure></div>

The following table describes the different states:

<table data-search="false"><thead><tr><th width="160">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Active</strong></td><td>The subscription is active and in use.</td></tr><tr><td><strong>Updating</strong></td><td>A business transaction is in progress for the subscription. This status applies to change orders submitted for the subscription.</td></tr><tr><td><strong>Suspending</strong></td><td>A suspension request or Suspend order is initiated for the subscription.</td></tr><tr><td><strong>Suspended</strong></td><td>The subscription is paused. You lose access to the service, but the subscription remains visible in the Marketplace. Suspended subscriptions expire at the end of the commitment period and don't renew automatically.</td></tr><tr><td><strong>Resuming</strong></td><td>A reactivation request or Resume order is initiated for the suspended subscription.</td></tr><tr><td><strong>Terminating</strong></td><td>A termination order has been created for the subscription.</td></tr><tr><td><strong>Terminated</strong></td><td><p>The vendor has completed the termination order, and the </p><p>subscription is now terminated.</p></td></tr><tr><td><strong>Expired</strong></td><td>The subscription has reached the end of its commitment term or contract without renewal.</td></tr></tbody></table>
