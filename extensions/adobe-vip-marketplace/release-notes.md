---
description: >-
  This page outlines the latest updates, improvements, and fixes to the
  integration between the SoftwareOne Marketplace and the Adobe VIP Marketplace.
---

# Release Notes

## Release Date: 8 October 2025

### Subscription Templates for Adobe VIP Marketplace

Adobe VIP Marketplace subscriptions now include **Subscription Templates**, providing clear, plain-language descriptions of each subscription’s current state and what will occur at renewal.

This enhancement gives customers better visibility into renewal outcomes, including whether a subscription will renew automatically (with the quantity that will be renewed) or expire at the anniversary date.

By adopting Subscription Templates, Adobe VIP Marketplace delivers a more transparent and predictable subscription experience.

***

## Release Date: 10 September 2025

### Self-Service Reseller Transfers

With this release, reseller transfers can now be completed directly in the Purchase Wizard, eliminating the need for a support ticket.&#x20;

You can change your reseller through the Marketplace Platform by providing your administrator's email address and the reseller code from the Adobe Admin Console. For detailed instructions, see [Transfer Your Adobe Reseller](reseller-transfer.md).

### Agreement Sync Improvements

The Agreement Sync process is more behind-the-scenes, but no less important to the day-to-day quality of life for users. The Agreement sync keeps our Marketplace up to date with changes that may occur at Adobe, but that we may not be aware of in the SoftwareOne Marketplace.

With this release, we improve this sync to include the following:

1. Automatically update Agreements when a 3-year commitment starts or ends.
2. Automatically update pricing in Subscriptions when a customer starts or finishes a 3-year commitment or renews their Agreement (goes past their anniversary date).
3. Automatically updates the quantities of Subscriptions after changes are made outside of the SoftwareOne Marketplace.
4. Automatically terminate Subscriptions that are expired or inactive at Adobe.
5. Automatically Terminate Agreements for customers that have performed a reseller transfer away from SoftwareOne.
6. \+ more

Lastly, in the Parameters tab of Agreements and Subscriptions, the "Last Sync Date" parameter indicates when the Agreement or Subscription was last synced with Adobe.

***

## Release Date: 10 July 2025

### Ordering end-of-sale items no longer fails

In this release, we have resolved an issue that occurred when increasing the quantity of end-of-sale items in a change order. Historically, these orders would fail in the SoftwareOne Marketplace, even if the order itself succeeded at Adobe.

This was due to the fact that once the order completes at Adobe, the Adobe extension then attempts to update the renewal quantity of the subscription to reflect the new desired quantity. End-of-sale items at Adobe cannot have their renewal quantities modified, though, and the attempt failed. This then caused the order in the SoftwareOne Marketplace to fail.

This issue has now been resolved. If the Adobe extension is unable to update the renewal quantity, then the order will now complete successfully. You will notice, however, that the quantity of the Subscription item in the SoftwareOne Marketplace remains the same as it was before the order was placed.

To view the new current quantity of the Subscription, you can check the "Current quantity" Parameter of the Subscription in the SoftwareOne Marketplace.

***

## Release Date: 9 July 2025

### Terminating Expired Subscriptions

When terminating a subscription that has already expired at Adobe, orders would get stuck in Processing status.

This issue is now resolved and termination orders placed against already expired subscriptions will now complete successfully resulting in Termination of the given Subscription in the SoftwareOne Marketplace.

***

## Release Date: 7 July 2025

### Delayed Orders Removed

Delayed orders have been removed from the Adobe extension. Previously, when a change or termination order was placed within 4 days of the customer's anniversary date, the order would be delayed until after the anniversary date.

This has now changed. Change, configuration, and termination orders can now be placed up to 24 hours prior to the anniversary date. Attempting to place an order within 24 hours of the anniversary date will result in an error in the Purchase Wizard. If the order is placed directly through the SoftwareOne Marketplace API, the order will be marked as failed.

### Termination Orders and Returns

Since the introduction of configuration orders to turn auto-renewal on or off, termination orders can now be used for a single purpose: to return the entire quantity of a subscription.

A termination order can now only be placed against a subscription or agreement if the entire quantity of the affected subscriptions can be returned at Adobe. If a subscription has licenses that are outside of the return window, then that subscription cannot be terminated. Instead, use a configuration order to disable auto-renewal.

{% hint style="info" %}
Note that change orders can still be used to make partial quantity returns as long as the quantity to return matches the entire amount of a line item on an order that is still within the 14-day return window.
{% endhint %}

### New Accounts and 3-year Commitments

When creating a new account with a 3-year commitment, the Adobe extension will now wait until the customer has accepted the 3-year commitment invitation before placing the order with Adobe. This ensures that the initial order is placed at the higher discount level provided by the commitment.

In addition, when preparing an order for a new account, the Adobe extension will validate the items in the order to ensure they all contribute to the 3-year commitment minimum quantities to avoid the order being placed at a lower (non-3yc) discount level.

### Subscription Adjustment Sequence Improvements

When a customer has a 3-year commitment, it is important when processing an order to ensure that the customer's quantities remain above the minimum quantities required for their 3-year commitment.

To this end, we have introduced two additional capabilities:

1. When an order is placed against a 3-year commitment, the order is validated to ensure that the combined changes that the order will make will still satisfy the minimum quantities.
2. When an order is fulfilled against a 3-year commitment, subscriptions with quantity increases are processed first, and then decreases are processed second. This ensures that the total quantities never go below the minimum quantities which would cause order failure.

***

## Release Date: 18 June 2025

### Multiple Currencies

A small number of customers have subscriptions in more than one currency in a single location. We now handle this as follows:

* Subscriptions in the same currency as the Agreement are activated during fulfilment of the Purchase Order. These subscriptions have auto-renewal enabled and are added to the Agreement.
* Subscriptions in a different currency to the Agreement are ignored. They are not added to the Agreement, and auto-renewal is switched off.

With this process, customers with multiple currencies in a single location will "consolidate" to a single currency at renewal.

***

## Release Date: 20 May 2025

### Notifications

Adobe VIP Marketplace notifications are now sent through the new Notifications module in the SoftwareOne Marketplace. This allows you do manage your notification settings for Adobe VIP Marketplace in the Notifications module.

To manage your notification preferences, click here: [https://portal.platform.softwareone.com/administration/settings/profile/notifications](https://portal.platform.softwareone.com/administration/settings/profile/notifications)

***

## Release Date: 25 March 2025

### Global Customer Improvements

In this release, we improved the creation of Agreements and Subscriptions for global customers:

* Agreement parameters now reflect the correct details of each deployment location.
* Inactive subscriptions at Adobe are ignored when creating the SoftwareOne Marketplace Subscriptions for each deployment location

### Other improvements

* One-time purchases are now excluded from Purchase Orders in the SoftwareOne Marketplace. These items were causing issues when completing those orders.

***

## Release Date: 15 January 2025

### Global Customer Support

Global Customers are now supported by the SoftwareOne Marketplace:

* Global customers can now be migrated from VIP to VIP Marketplace.
* Global customers can be activated in the SoftwareOne Marketplace. The main account and each deployment location will have its own Agreement.
* You can now place orders against the main account or any deployment location.
* Billing update to support global customers.

***

## Release Date: 15 October 2024

### Order Processing Before Renewal <a href="#title-text" id="title-text"></a>

In this release, we added functionality for "delayed orders". In the few days leading up to renewal, changes made to subscriptions at Adobe may not be reflected after renewal.

To ensure a predictable outcome for these orders, we will now delay them until after the renewal has taken place.

***

## Release Date: 26 September 2024

### Order Processing for Quantity Reductions

In this release, we improved quantity decreases of subscriptions to ensure any returnable orders are returned where possible.

* Attempts to reduce the quantity of subscriptions prior to the final two weeks before renewal require returnable orders in order to be processed.
* Attempts to reduce the quantity of subscriptions within the final two weeks before renewal only set the renewal quantity for the next renewal.

### Other improvements

* Improved setting of autorenewal for subscriptions when a customer account is activated in the SoftwareOne Marketplace.&#x20;
* Improved handling of customer accounts that are marked as inactive by Adobe. We now show an appropriate error message when trying to activate an Adobe VIP Marketplace account that has been disabled by Adobe.
* Other various minor improvements

***

## Release Date: 22 May 2024

### Support for Adobe VIP Marketplace Products

With VIP Marketplace Program, you can purchase Adobe subscriptions via self-service on the Marketplace Platform, and take advantage of volume discounts and automated renewals.

To learn about the VIP Marketplace program, see [Adobe VIP Marketplace](./).&#x20;
