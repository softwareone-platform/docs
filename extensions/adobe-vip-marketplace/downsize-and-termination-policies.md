---
description: Learn about our returns, downsizing, and termination policies.
---

# Downsize, termination, and return policies

The SoftwareOne Marketplace allows you to manage your Adobe VIP subscriptions, including adjusting license quantities, disabling auto-renewal, or terminating subscriptions.&#x20;

This article explains how downsizing, termination, auto-renewal, and returns work, and the key rules you must follow when making changes.

## Key terms

The following are some of the key terms related to Adobe VIPM subscriptions in the Marketplace:

* **Downsize** – Downsizing a subscription involves reducing the number of licenses while keeping at least one license active. A downsize reduces active licenses immediately if returnable orders are available and reduces the renewal quantity for the next term.
* **Auto-renewal** – Auto-renewal controls whether a subscription automatically renews at the end of its term.&#x20;
  * If auto-renewal is enabled, the subscription renews automatically.
  * If auto-renewal is disabled, the licenses remain active until the next anniversary date and then expire. After expiry, licenses are no longer available to users. Any users with licenses assigned after the anniversary date lose access.
* **Termination** – Terminating a subscription means canceling it entirely and returning its entire license quantity. Termination is only available if the subscription's full license quantity is eligible for return within the 14-day return window.
* **Returnable order** – A returnable order is any new or renewal order placed within the 14-day return window. You can return such orders without a charge during the 14-day return window after the order is completed.

## Return policy

Returns for Adobe VIP Marketplace subscriptions are only allowed within 14 days of purchase or renewal. This means that a subscription that has just been ordered or renewed can still be returned in full if it's within the 14-day return window.

* Full subscription returns are done by terminating the subscription or agreement.
* Partial returns are done by downsizing.

After this period, returns are not allowed. Only auto-renewal settings can be changed by placing a configuration order in the SoftwareOne Marketplace.&#x20;

### Full return (termination)

You can return a full subscription within the 14-day return window by submitting a termination order for the full subscription quantity.

When the termination order is processed, the subscription's quantity is reduced to zero (`0`) and its status changes to **Terminated**. Auto-renewal is also disabled. In the Adobe Admin Console, the subscription is removed, and any affected licenses immediately become unavailable to users.

For more details, see [Terminate and return licenses](tutorials-and-videos/terminate-adobe-subscription.md) and [Cancel entire agreement](tutorials-and-videos/terminate-all-adobe-subscriptions.md).

### Partial return (downsize)

You can return eligible subscription quantities within the 14-day return window by submitting a change order.

Partial returns are only allowed if the total number of licenses matches the full quantity of the order line item. For example, if an order contains 5 Photoshop for Teams licenses, you must return all 5 licenses from that line item. When the change order is processed, the affected licenses immediately become unavailable to users.&#x20;

For more details, see [Downsize subscription](tutorials-and-videos/downsize-adobe-subscription.md).

### Return after renewal

If a subscription has been renewed, you can return it within the 14-day return window.&#x20;

You can return the full renewed subscription by submitting a termination order. To return a partial quantity, submit a change order to downsize the subscription in the SoftwareOne Marketplace.

When the order is processed, all affected licenses are removed immediately. For more details, see [Return renewal order](tutorials-and-videos/return-renewal-order.md).

## Downsize policy

You can downsize a subscription by placing a change order in the SoftwareOne Marketplace.

A downsize adjusts your current licenses (if a return is processed) and updates the renewal quantity for the next term. To view current and renewal quantities, check the **General** tab of the subscription.

### Downsize with returnable orders

If your subscription includes returnable orders, you can only downsize by quantities that match the sum of orders within the return window.&#x20;

When you perform a downsize in this scenario, Adobe processes a return for the affected licenses, and they immediately become unavailable to your users.

Additionally, the subscription's renewal quantity is reduced to match the new license quantity after the return is processed.

If your requested reduction quantity doesn't match the quantity of one or more returnable orders, the system prevents the reduction from being processed and suggests a valid returnable quantity.

### Downsize without returnable orders

If a subscription doesn't contain returnable orders, only the renewal quantity is reduced. This ensures that at the next renewal, only the reduced quantity of licenses is renewed.

### Example scenario

The following example illustrates how downsizing works in the platform. Assume the following:

1. You own 10 Photoshop for Teams licenses, which were ordered 30 days ago and are therefore outside the return window.
2. You ordered an additional 4 Photoshop for Teams licenses 10 days ago, which are within the return window.
3. You ordered another 3 Photoshop for Teams licenses 3 days ago, which are also within the return window.

Based on this information, you currently own a total of 17 licenses.&#x20;

* If you want to return the 4 additional licenses and downsize by 4, the system will process the return.
* If you want to downsize by 7, the orders for the 4 additional licenses and the 3 additional licenses will be returned.
* If you want to downsize by 6, no single order (or combination of orders) matches the required quantity of 6, and the platform blocks the change and suggests a valid returnable quantity.

## Auto-renewal policy

You can change auto-renewal settings by placing a configuration order in the SoftwareOne Marketplace.

If auto-renewal is enabled, the subscription renews automatically. If disabled, the subscription remains active until the next anniversary date and then expires. For details on turning off auto-renewal, see [Disable auto-renewal](tutorials-and-videos/disable-auto-renewal.md).

## Related topics

For step-by-step instructions on performing returns, downsizing, or termination actions, see the [Adobe VIP Marketplace Tutorials](tutorials-and-videos/).
