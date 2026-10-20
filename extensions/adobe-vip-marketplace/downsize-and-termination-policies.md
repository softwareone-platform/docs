---
description: Learn about our returns, downsizing, and termination policies.
---

# Downsize, termination, and return policies

You can manage your Adobe VIP Marketplace subscriptions in the SoftwareOne Marketplace: reduce license quantities, turn auto-renewal on or off, and terminate subscriptions. This article explains how reductions, returns, terminations, and auto-renewal work, and the rules that apply when you make changes.

### Key terms

* **Current quantity** – The number of licenses you hold now and can assign to users.
* **Renewal quantity** – The number of licenses that will renew on your anniversary date.
* **Return window** – 14 days from the date of a new or renewal order. Licenses bought or renewed in the last 14 days are _returnable_.
* **Reduce (downsize)** – Lowering a subscription's quantity with a change order, while keeping at least one license.
* **Termination** – Canceling a subscription with a termination order, which returns all of its licenses. This is different from reducing: a reduction always leaves at least one license. A termination is only possible when every license on the subscription is still returnable.
* **Auto-renewal** – Whether a subscription renews on your anniversary date. If auto-renewal is off, the licenses stay active until the anniversary date and then expire.

You can see the **Current quantity** and **Renewal quantity** of a subscription on its **General** tab.

### Returns

You can return any number of licenses that you bought or renewed in the last 14 days, as long as they aren't in use. You don't have to return a whole order.

* To return **part** of a subscription, reduce its quantity with a change order. For more details, see [Reduce Adobe license quantity](tutorials-and-videos/downsize-adobe-subscription.md).
* To return **all** of a subscription, terminate it. For more details, see [Terminate and return Adobe licenses](tutorials-and-videos/terminate-adobe-subscription.md) and [Cancel Adobe agreement](tutorials-and-videos/terminate-all-adobe-subscriptions.md).

Returned licenses become unavailable to users immediately. You receive a credit for them at the price in effect when the return is processed. This price may differ from the price you originally paid.

#### Which licenses can be returned

Licenses are returnable when they come from a new or renewal order that:

* was placed in the last 14 days,
* is complete, and
* was placed on or after the subscription's most recent renewal.

When you return licenses, they are taken from your oldest returnable order first.

#### What cannot be returned

* Licenses bought more than 14 days ago.
* Licenses bought before your most recent renewal, even if that was less than 14 days ago.
* Mid-term upgrades.
* Consumables (for example, Adobe Sign transactions), Stock Credit Packs, Acrobat license packs, and minimum-order-quantity (MOQ) offers.
* Orders placed in Adobe VIP before you migrated to VIP Marketplace.

### Reduce a subscription

When you reduce a subscription's quantity, each product on your change order is handled in one of two ways. The following table describes the two outcomes:

| Outcome                | When it happens                                                                                                          | Current quantity                      | Renewal quantity | Credit |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------- | ---------------- | ------ |
| **Returned**           | You bought or renewed at least as many licenses as you're removing in the last 14 days, and the product can be returned. | Reduced immediately                   | Reduced to match | Yes    |
| **Reduced at renewal** | You're removing more licenses than you bought or renewed in the last 14 days, or the product cannot be returned.         | Unchanged until your anniversary date | Reduced          | No     |

A product is never split between the two: either the whole reduction is returned, or the whole reduction applies at renewal. If your order has several products, some can be returned while others are reduced at renewal.

Your order completes in both cases. To check which one happened, open the subscription's **General** tab:

* **Returned** – The **Current quantity** has gone down.
* **Reduced at renewal** – The **Current quantity** is unchanged, and only the **Renewal quantity** has gone down. Your licenses stay available to users until your anniversary date.

#### Example

You hold 17 Photoshop for Teams licenses:

1. 10 were bought 30 days ago. They are outside the return window.
2. 4 were bought 10 days ago. They are returnable.
3. 3 were bought 3 days ago. They are returnable.

So 7 licenses are returnable. The following table describes what happens when you reduce by different quantities:

| You reduce by | Outcome                                         | Current quantity | Renewal quantity | Credit for |
| ------------- | ----------------------------------------------- | ---------------- | ---------------- | ---------- |
| 4             | Returned (the 4 from 10 days ago)               | 13               | 13               | 4 licenses |
| 6             | Returned (the 4, then 2 of the 3)               | 11               | 11               | 6 licenses |
| 7             | Returned (all 7)                                | 10               | 10               | 7 licenses |
| 10            | Reduced at renewal (more than the 7 returnable) | 17               | 7                | None       |

#### 3-year commitment

If you have a 3-year commitment, you cannot reduce your licenses below your committed minimum. A reduction that would take you below it is refused.

### Termination

A termination cancels a subscription and returns every license on it. It's only possible when **all** of the subscription's licenses are still returnable, for example, when all of them were bought in the last 14 days.

If any license on the subscription is outside the return window, the termination order is refused. Instead, turn off auto-renewal with a configuration order, so the subscription expires on your anniversary date. For more details, see [Disable Adobe auto-renewal](tutorials-and-videos/disable-adobe-auto-renewal.md).

When a termination is processed:

* The subscription is canceled, and its status changes to **Terminated**.
* Auto-renewal is turned off.
* In the Adobe Admin Console, the subscription is removed, and its licenses become unavailable to users immediately.

When a termination returns several orders, they're returned one after another, so the order can stay in **Processing** a little longer.

### Returns after a renewal

When a subscription renews, the renewal order can be returned for 14 days, like any other order:

* To return part of the renewal, reduce the subscription's quantity. Licenses are taken from the renewal order and from any orders placed after it.
* To return all of it, terminate the subscription. This only works if every license on the subscription came from the renewal or later orders.

Licenses bought before the renewal cannot be returned, even if they were bought less than 14 days ago. For more details, see [Return Adobe renewal order](tutorials-and-videos/return-adobe-renewal-order.md).

### Auto-renewal

You can turn auto-renewal on or off with a configuration order in the SoftwareOne Marketplace.

If auto-renewal is on, the subscription renews on your anniversary date at its **Renewal quantity**. If it's off, the subscription stays active until your anniversary date and then expires. For more details, see [Disable Adobe auto-renewal](tutorials-and-videos/disable-adobe-auto-renewal.md).

### Related topics

For step-by-step instructions, see the [Tutorials](tutorials-and-videos/). For error messages, see [Common error messages](common-error-messages.md).
