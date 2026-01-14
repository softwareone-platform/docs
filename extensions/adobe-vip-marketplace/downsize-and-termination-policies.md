---
description: Learn about our downsizing and termination policies.
---

# Downsize and Termination Policies

The Marketplace Platform allows you to manage your Adobe VIP Marketplace software subscriptions. This includes the ability to reduce or downsize the number of licenses or completely cancel/terminate a subscription.&#x20;

This topic explains how downsizing and termination work and the key points to keep in mind before requesting a downsize or termination.

## Key terms

The following are some of the key terms related to Adobe VIPM subscriptions in the Marketplace Platform:

* **Downsize** - Downsizing a subscription involves reducing the number of licenses while keeping at least one license active.
* **Disable autorenewal** - Disabling autorenewal for a subscription means that its licenses will remain active until the next anniversary date upon which it will expire, and the licenses will no longer be available to users. Any users with licenses assigned after the anniversary date will lose access.
* **Terminate** - Terminating a subscription means canceling it entirely and returning the entire quantity of licenses. Termination is only available if the subscription's entire quantity of licenses are still within the return window (14 days) and can be returned.
* **Returnable order** - Any new or renewal order placed within the 14-day return window. Such orders can be returned without a charge at any time during the 14 days after the order completes.

## How downsizing works

To perform a downsize, use the purchase wizard in the SoftwareOne Marketplace to place a change order for an existing agreement or subscription.

Performing a downsize may affect your current quantity of licenses (if a return is processed) and will also affect the renewal quantity for the next renewal. Information about the current quantity and renewal quantity is available on the General tab of the subscription in the SoftwareOne Marketplace.

### Downsizing a subscription with returnable orders

When a subscription has returnable orders, you may only downsize by quantities that match the sum of orders that are within the return window. When you perform a downsize in this scenario, Adobe will process a return for the affected licenses, and they will immediately become unavailable to your users.

In addition, the renewal quantity of the subscription will be reduced to match the new quantity of licenses after the return as been processed.

In cases where your requested reduction quantity doesn't match the quantity of one or more returnable orders, the system will prevent the reduction from being processed and suggest a valid quantity that can be returned.

### Downsizing a subscription without returnable orders

When a subscription does not have any returnable orders, only the renewal quantity of the subscription will be reduced. This ensure that at the next renewal, only the reduced quantity of licenses is renewed.

### Example scenario

The following example illustrates how downsizing works in the platform. For this example, assume the following:

1. You own 10 licenses of Photoshop for Teams, which were ordered 30 days ago and are therefore outside the return window.
2. You ordered an additional 4 licenses of Photoshop for Teams 10 days ago, which are within the return window.
3. You ordered another 3 licenses of Photoshop for Teams 3 days ago, which are also within the return window.

Based on this information, you currently own a total of 17 licenses for Photoshop for Teams.&#x20;

* If you wish to return the 4 additional licenses and downsize by 4, the system will process the return.
* If you wish to downsize by 7, the orders for the 4 additional licenses, as well as the 3 additional licenses, will be returned.
* If you request to downsize by 6, no single order (or combination of orders) matches the required quantity of 6, and the system will prevent the change and suggest a valid quantity that can be returned.

## How disabling auto-renewal works

To disable (or enabled) autorenewal for a subscription, use the configuration wizard in the SoftwareOne Marketplace to place a configuration order for an existing subscription.

When autorenewal is disabled for a subscription, the subscription remains active until the next anniversary date upon which it expires.

For more information on placing a configuration order, see [manage-automatic-renewals.md](../../modules-and-features/marketplace/subscriptions/manage-automatic-renewals.md "mention").

## How termination works

You can terminate a subscription if the entire quantity of its licenses are still within the return window.&#x20;

In this case, all licenses under the given subscription will immediately become unavailable to your users.

For more information on placing a termination order, see [terminate-a-subscription.md](../../modules-and-features/marketplace/subscriptions/terminate-a-subscription.md "mention").
