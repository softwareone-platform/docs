# Downsize and termination policies

The Marketplace Platform allows you to manage your Adobe VIP Marketplace software subscriptions. This includes the ability to reduce or downsize the number of licenses or completely cancel/terminate a subscription.&#x20;

This topic explains how downsizing and termination work and key points to keep in mind before requesting a downsize or termination.

## Concepts

The following are some of the key terms related to Adobe VIPM subscriptions in the Marketplace Platform:

* **Downsize** - Downsizing a subscription involves reducing the number of licenses while keeping at least one license active.
* **Terminate** - Terminating a subscription means canceling it entirely and disabling auto-renewal. When a subscription is terminated, licenses for the terminated subscription remain available in the [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html) until the renewal date.
* **Returnable orders** - This implies any new or renewal orders placed within the 14-day return window. Such orders can be returned without a charge at any time during the 14 days after the order is placed.
* **Weeks 1 to 50** - Weeks 1 to 50 are the weeks of the year starting at the renewal date and ending 14 days before the next renewal date.
* **Weeks 51 and 52** - Weeks 51 and 52 are the weeks of the year starting 14 days before the renewal date and ending on the renewal date.

## How downsizing and terminations work

### Standard process (Weeks 1 to 50)

You can return licenses if your order falls within the 14-day return window. In these cases, Adobe will process a return for the affected licenses. If your order is outside the 14-day return window, the renewal quantity of the subscription will be reduced instead.&#x20;

In cases where your requested reduction doesn't match the quantity of one or more returnable orders, the system will prevent the reduction from being processed and display a message.

### Approaching renewal (Weeks 51 to 52)

As you approach the renewal period, specifically during the last two weeks (weeks 51 and 52), any requests to downsize or terminate will reduce the renewal quantity of your licenses. In such cases, no returns will be processed through Adobe.

Should you choose to terminate your subscription, auto-renewal will be disabled. It means that your subscription won't renew after the current term ends.

{% hint style="success" %}
## Summary

* Licenses can be returned without charge within 14 days of placing a new or renewal order; after that, only the subscription’s renewal quantity is reduced. Your purchased licenses will remain active until the renewal date.
* For returns within the 14-day window, you must return the entire order or the full quantity of licenses purchased. For example, if you ordered 10 licenses for Creative Cloud All Apps, you must return all 10 licenses. If the quantity doesn't match, the platform displays a message. See [Common error messages](broken-reference) to learn more.
* Terminating a subscription automatically cancels auto-renewal.
{% endhint %}

## Example scenario

The following example illustrates how downsizing works in the platform. For this example, assume the following:

1. You own 10 licenses of Photoshop for Teams, which were ordered 30 days ago and are therefore outside the return window.
2. You ordered an additional 4 licenses of Photoshop for Teams 10 days ago, which are within the return window.
3. You ordered another 3 licenses of Photoshop for Teams 3 days ago, which are also within the return window.

Based on this information, you currently own a total of 17 licenses for Photoshop for Teams.&#x20;

* If you wish to return the 4 additional licenses and downsize by 4, the system will process the return.
* If you wish to downsize by 7, the orders for the 4 additional licenses as well as the 3 additional licenses will be returned.
* If you request to downsize by 6, but no single order (or combination of orders) matches the required quantity of 6, the system will prevent the change and suggest a valid quantity that can be returned.
