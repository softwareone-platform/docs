# Subscription States

This topic describes the subscription states for license-based New Commerce and Legacy subscriptions. It also describes how these subscription states are represented within the Marketplace Platform.

## NCE subscription states <a href="#license-based-new-commerce-subscription-states" id="license-based-new-commerce-subscription-states"></a>

NCE subscriptions can be in one of these states: **Active**, **Suspended**, **Expired**, **Disabled**, or **Deleted**.

### Active

**Active** is the default state for an NCE subscription. When the subscription is active, you can access and use the services. Additionally:

* Administrators can access service data and properties.
* Partners can access and make changes to the subscription properties.
* Transacting partners continue to be billed.

### Suspended

Partners can suspend (previously known as ‘Pause’) a subscription to temporarily make the services unavailable to customers. When the subscription is suspended:

* Customers can no longer access and use services.
* Administrators can access service data and properties.
* Transacting partners continue to be billed.
* Partners can reactivate the subscription before the end of its commitment term.
* Partners can cancel the subscription if it's still within the 7-day transaction window.
* If the suspended subscription reaches its end date while still in the suspended state, it moves to a **30-day disabled state**.

### Expired

The **30-day expired state** follows the end of an **Active** subscription. A previously active subscription will enter this state if auto-renew is turned off and the terms end. In these 30 days:

* Users can access files and services.
* Administrators can access data.
* Transacting partners aren't billed.
* Subscriptions can’t be reactivated.

After 30 days in the expired state, the subscription moves to a **90-day disabled state**.

### Disabled

A **30-day disabled state** follows the end of a suspended subscription. In this state:

* Partners that suspend their subscription leading to the term end will find their suspended subscription moved to this 30-day disabled state.
* After 30 days in the disabled state, the subscription moves to a 90-day disabled state (120 days disabled in total).
* Users can't access files and services, and only administrators can access the data.
* Transacting partners aren't billed.
* Subscriptions can't be reactivated.

The **90-day disabled state** follows the 30-day **Expired** or a 30-day **Disabled** state:

* 90-day disabled state **-** Data is retained for 90 days after the end of the previous state.
* Users can't access files and services, and only administrators can access the data.
* Transacting partners aren't billed.
* Subscriptions can't be reactivated.

### Deleted

After the subscription passes through the 90-day disabled state, it stays deleted. However:

* The subscription is non-recoverable.
* All customer data associated with the subscription is handled per applicable data retention policies.
* After a subscription is canceled, there's a 90-day post-canceled window where:
  * If the partner purchases the same product/SKU equivalent to the one canceled, customer data and user license assignment settings are automatically restored.
  * If a new purchase is made with a lower number of licenses, customer data and user license assignment settings are still retained. The partner should manage them appropriately.
  * After the 90 days, these actions are no longer allowed. The data is removed.
* Transacting partners aren't billed.
* Deleted subscriptions can't be reactivated.

## Legacy subscription states <a href="#license-based-legacy-subscription-states" id="license-based-legacy-subscription-states"></a>

Legacy subscriptions can be in one of these states: **Active**, **Suspended**, or **Deleted**.

### Active

**Active** is the default state for a legacy subscription. In this state:

* Partners can access and make changes to subscription properties.
* Customers can access and use services.
* Administrators can also access service data and properties.
* Transacting partners continue to be billed.

### Suspended

In the **Suspended** state:

* Partners suspend a subscription to temporarily make the services unusable to customers.
* Partners can reactivate the subscription before the end of the term.
* If the subscription is still suspended by the term's end, the subscription is deleted.
* Partners can only reactivate the subscription.
* Customers can no longer access and use services.
* Administrators can access service data and properties.
* Transacting partners aren't billed.

### Deleted

After 90 days in the suspended state, the subscription is deleted and non-recoverable.

## Subscription states in the Marketplace <a href="#subscription-states-withing-the-softwareone-marketplace" id="subscription-states-withing-the-softwareone-marketplace"></a>

The following table shows how various Microsoft subscription states are represented in the Marketplace Platform:

<table><thead><tr><th width="239">Product type</th><th>Microsoft states</th><th>Marketplace states</th></tr></thead><tbody><tr><td><p>License-based NCE</p><p>(example: Microsoft 365 / Dynamics 365)</p></td><td><ul><li>Active</li></ul><ul><li>Suspended</li><li>Expired</li><li>Disabled</li><li>Deleted</li></ul></td><td><ul><li>Active</li></ul><ul><li>Terminated</li><li>Expired</li><li>Terminated</li><li>Terminated</li></ul></td></tr><tr><td><p>License-based Legacy</p><p>(example: Microsoft 365 / Dynamics 365)</p></td><td><ul><li>Active</li><li>Suspended</li><li>Deleted</li></ul></td><td><ul><li>Active</li><li>Terminated</li><li>Terminated</li></ul></td></tr><tr><td><p>Usage-based</p><p>(example: Microsoft Azure)</p></td><td><ul><li>Active/Enabled</li><li>Deleted</li><li>Disabled</li></ul></td><td><ul><li>Active</li><li>Terminated</li><li>Terminated</li><li>Terminated</li></ul></td></tr><tr><td><p>Perpetual</p><p>(example: Perpetual Excel license)</p></td><td><ul><li>Active</li><li>Cancelled</li></ul></td><td><ul><li>Active</li><li>Terminated</li></ul></td></tr><tr><td><p>Software subscription</p><p>(example: Windows Server CAL 1yr)</p></td><td><ul><li>Active</li></ul><ul><li>Suspended</li><li>Expired</li><li>Disabled</li><li>Deleted</li></ul></td><td><ul><li>Active</li></ul><ul><li>Terminated</li></ul><ul><li>Expired</li></ul><ul><li>Terminated</li></ul><ul><li>Terminated</li></ul></td></tr></tbody></table>
