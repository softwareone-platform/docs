# Subscription States

The following diagram shows the possible states of a subscription and the transition between these states:

<figure><img src="../../../.gitbook/assets/state_diagram_subscription.png" alt=""><figcaption><p>Subscription state transition</p></figcaption></figure>

<table><thead><tr><th width="135">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The vendor has created the subscription, but the order has not been completed yet.</td></tr><tr><td><strong>Active</strong></td><td>The subscription is active and in use.</td></tr><tr><td><strong>Updating</strong></td><td><p>A business transaction is in progress for the subscription. </p><p></p><p>This status applies to change orders submitted for the subscription.</p></td></tr><tr><td><strong>Terminating</strong></td><td>A termination order has been created for the subscription through the Client Portal.</td></tr><tr><td><strong>Terminated</strong></td><td><p>The vendor has completed the termination order and the </p><p>subscription is now terminated.</p></td></tr><tr><td><strong>Deleted</strong></td><td>The draft subscription has been deleted by the vendor.</td></tr></tbody></table>
