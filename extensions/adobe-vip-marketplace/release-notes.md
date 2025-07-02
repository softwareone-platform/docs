---
description: >-
  This page outlines the latest updates, improvements, and fixes to the
  integration between the SoftwareOne Marketplace and the Adobe VIP Marketplace.
---

# Release Notes

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
