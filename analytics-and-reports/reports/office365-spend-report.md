---
description: Get detailed analysis of your Office365 spend.
---

# Office365 Spend Report

Office365 Consumption provides users with detailed Office365 spend analysis. The data is based on the billing data that is fetched daily.

Using Office365 Consumption, you can access multiple analytic reports and browse consumption cost information through interactive charts. The analysis is extended by leveraging information from the other Client Portal modules. You can also analyze spend per [Custom Group](../../spend-management/custom-groups/) or [Budget](../../spend-management/budgets/).

***

## Accessing Office 365 Consumption <a href="#how-to-access-office-365-consumption" id="how-to-access-office-365-consumption"></a>

**To access Office365 Consumption**

1. From the main menu, navigate to **Analyze** and select **Consumption overview**. The Consolidated Consumption page displays.
2. From the **View** menu, select **SaaS Office365 Consumption Details** or **Office365 Billing Consumption Details (Preview)**.

***

## Office365 Consumption <a href="#office-365-consumption" id="office-365-consumption"></a>

You can visualize and analyze your Office 365 EA and Office 365Simple spend.&#x20;

Each Azure Active Directory user and subscription is treated like a resource. You can assign it to a custom group, add tags, or split the quantity between different business units.

### SaaS Office365 Consumption Details Report <a href="#understand-the-saas-office365-consumption-details-report" id="understand-the-saas-office365-consumption-details-report"></a>

The **SaaS Office365 Consumption Details Report** report displays the cost or quantity data.

* The cost data always reports the initial monthly cost on the first day of the month and additional costs due to subscription updates on the day it happened. The cost data is calculated in a single currency.

<figure><img src="../../.gitbook/assets/image (187).png" alt=""><figcaption><p><strong>Monthly initial cost and subscription update cost</strong></p></figcaption></figure>



* The quantity data shows the maximum number of subscriptions by product subscription per month.

<figure><img src="../../.gitbook/assets/image (188).png" alt=""><figcaption><p><strong>Subscription quantity</strong></p></figcaption></figure>

***

### **Office 365Simple Multiple Agreements Tenant**

The cost data for the Office 365Simple Multiple Agreements Tenant uses the average price calculated in a single currency. The average price is calculated on the first day of the month and on every subscription update.&#x20;

To check the billing data per agreement, use the **Office365 Billing Consumption Details (Preview)** report or see the **Billing** tab under **Cloud Subscriptions**.

{% hint style="info" %}
**NOTE:** If your Office365 tenant has subscriptions in multiple currencies, the Client Portal will only display the consumption data in the default currency of the portal. Multicurrency calculations are not supported for Office365 consumption.&#x20;
{% endhint %}

### **Office 365 EA Tenant**

The cost data for Office365 EA Tenant uses the average price set manually in the Price List.

If the price for a subscription is not set, an information banner is displayed as shown in the following image:

<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption><p><strong>Missing prices information banner</strong></p></figcaption></figure>

The price in the Price List Center is set for every subscription per month and the average calculation has to be done manually. All missing prices are visible under **Missing Prices**. If the historical quantity data is available, the cost data is recalculated starting from the **Effective Date**.

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption><p><strong>Setting missing price</strong></p></figcaption></figure>

### **Office 365 Tenant with Mixed Purchase Agreements**

The cost data for an Office 365 Tenant with mixed purchase agreements (that is, Office 365Simple and EA) uses an average price calculation based on the **Office 365Simple prices** only.

The Client Portal doesn't support setting custom prices for the subscriptions purchased through the Office 365 EA agreement. For Office 365 Tenants with mixed purchase agreements, an information banner is displayed.

<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption><p><strong>Mixed Purchase Agreements Banner</strong></p></figcaption></figure>

## Understand the Office 365 Resource Spend <a href="#understand-the-office-365-resource-spend" id="understand-the-office-365-resource-spend"></a>

Azure Active Directory users and subscriptions are treated like **resources**. Azure Active Directory user **resource** cost, is a sum of costs of all subscriptions assigned to this user.

Subscription **resource** cost is the cost of all subscriptions that are not assigned to any Azure Active Directory user (Subscription **resource** has a name set to Subscription name and “Unassigned Pool” suffix).

<figure><img src="../../.gitbook/assets/image (193).png" alt=""><figcaption><p><strong>Office 365 Resource Spend</strong></p></figcaption></figure>
