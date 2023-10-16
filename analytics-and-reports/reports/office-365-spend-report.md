---
description: Gain detailed analysis of your Office 365 spend.
---

# Office 365 Spend Report

### What is Office 365 Consumption?   <a href="#what-is-office-365-consumption-in-pyracloud" id="what-is-office-365-consumption-in-pyracloud"></a>

Office 365 Consumption provides users with detailed Office 365 spend analysis. The data is based on billing data fetched daily.

Users can access multiple analytic reports and browse consumption cost information in easy-to-use interactive charts. The analysis is extended by leveraging information from the other modules. Users can analyze spend per [Custom Group](broken-reference) or per [Budget.](../../spend-management/budgets/working-with-budgets.md)

***

### Accessing Office 365 Consumption <a href="#how-to-access-office-365-consumption" id="how-to-access-office-365-consumption"></a>

To access Office 365 Consumption:

1. From the main menu, navigate to **Analyze** and select **Consumption overview**.&#x20;
2. Select **SaaS Office365 Consumption Details** or **Office365 Billing Consumption Details (Preview)** from the menu.

***

### Office 365 Consumption <a href="#office-365-consumption" id="office-365-consumption"></a>

You can visualize and analyze your Office 365 EA and Office 365Simple spend. Each Azure active directory user and subscription is treated like a **resource**. You can assign it to a custom group, add tags or split the quantity between different business units.

#### Understand the “SaaS Office365 Consumption Details” Report <a href="#understand-the-saas-office365-consumption-details-report" id="understand-the-saas-office365-consumption-details-report"></a>

The Office365 Consumption Details Report displays the Cost or the Quantity data.

The Cost data always reports the initial monthly cost on the first day of the month and additional costs due to subscription updates on the day that it happened. Cost data is calculated in the single currency.

<figure><img src="../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>



The Quantity data shows maximum number of subscriptions by product subscription per month.

<figure><img src="../../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

***

**Office 365Simple Multiple Agreements Tenant**

The Cost data for Office 365Simple Multiple Agreements Tenant uses the average price calculated in a single currency. The average price is calculated at the first day of the month and on every subscription update. To check the billing data per agreement, please use “Office365 Billing Consumption Details (Preview)” report or Cloud Subscriptions (see Cloud Subscription Billing)

{% hint style="info" %}
**NOTE:** If there are multiple buying currencies for a single Office365 tenant – the cost is calculated using the default currency and the most up-to-date exchange rates are applied. The exchange rates are updated daily by SoftwareONE using an external public rates source.
{% endhint %}

**Office 365 EA Tenant**

The Cost data for Office 365 EA Tenant uses the average price set manually in the Price List.

If the price for a subscription is not set, an information banner will be displayed.

<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

The price in Price List Center is set for every subscription per month and average calculation has to be done manually. All missing prices are visible in the missing prices Tab. If historical Quantity data is available, Cost data will be recalculated starting from “Effective Date”.

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

**Office 365 Tenant with Mixed Purchase Agreements**

The cost data for an Office 365 Tenant with mixed purchase agreements (i.e. Office 365Simple and EA) uses an average price calculation based on the **Office 365Simple prices** only.

We do not currently support setting custom prices for the subscriptions bought through Office 365 EA agreement. For Office 365 Tenants with mixed purchase agreements, an information banner will be displayed.

<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

#### Understand the Office 365 Resource Spend <a href="#understand-the-office-365-resource-spend" id="understand-the-office-365-resource-spend"></a>

Azure Active Directory users and subscriptions are treated like **resources**.

Azure Active Directory user **resource** cost, is a sum of costs of all subscriptions assigned to this user.

Subscription **resource** cost is the cost of all subscriptions that are not assigned to any Azure Active Directory user (Subscription **resource** has a name set to Subscription name and “Unassigned Pool” suffix).

<figure><img src="../../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>
