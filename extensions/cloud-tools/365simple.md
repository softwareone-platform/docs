---
description: Learn about the 365Simple dashboard.
---

# 365Simple

The 365Simple dashboard provides an overview for clients using SoftwareOne’s 365Simple service.&#x20;

You can access the dashboard by navigating to the main menu of the Client Portal and selecting  **Cloud tools > 365Simple**.

## Dashboard interface <a href="#selecting-your-tenant" id="selecting-your-tenant"></a>

The dashboard provides a single point of access to other areas of the platform, such as invoices and user administration. Through the dashboard, you can also view your billing information, product usage, and more.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>365Simple dashboard</p></figcaption></figure>

The dashboard consists of the following sections:

* [Select Microsoft Tenant](365simple.md#select-microsoft-tenant)
* [Billing cycle and product subscription](365simple.md#billing-information)
* [Product usage and subscription assignment](365simple.md#product-usage-subscriptions-assignment)
* [Recommendations and articles](365simple.md#service-recommendations-articles)
* [365Simple Support tickets](365simple.md#help-and-support-overview)
* [Top 5 subscription changes](365simple.md#recent-subscription-changes)
* [Recent news from Microsoft](365simple.md#recent-news-from-microsoft)

### Select Microsoft Tenant

If you have multiple Microsoft tenants, you'll see an option to switch between tenants.&#x20;

When you switch tenants, the widget values in the dashboard change accordingly. As tenants are permission-based, you may not see all available customer tenants.  Also, widgets like Invoices and Add users are based on permissions. If you are unable to view the sections, contact your administrator to check your permissions.

### Billing cycle and product subscription <a href="#billing-information" id="billing-information"></a>

This widget displays billing cycles from the past 90 days. It will usually contain the last 3 billing cycles, but it may also contain 4 if the billing cycle spans across two months.

If you hover over each billing cycle, you will see the billing date range, currency, subscription breakdown and total amount. Clicking the section opens the **My Subscriptions** page where you can see more details.

{% hint style="info" %}
The section displays the default CSP agreement if you have multiple CSP agreements. Switching between agreements is currently not supported.
{% endhint %}

### Product usage and subscription assignment <a href="#product-usage-subscriptions-assignment" id="product-usage-subscriptions-assignment"></a>

The **Product Usage** and **Top 5 Assigned Subscriptions** show information per Microsoft tenant (as noted on the yellow label within each widget). Viewing the usage and subscription assignments per agreement is impossible as the vendor does not support the functionality.

* The **Product Usage** section provides an overview of the active and inactive licenses and highlights opportunities to adjust the use vs. cost ratio. Clicking on the widget opens up 365Analytics.&#x20;
* The **Top 5 Subscriptions By Assigned** section can be used to evaluate subscription utilization and accompanying costs. Clicking on the widget opens up a full consumption report.

### Recommendations and articles <a href="#service-recommendations-articles" id="service-recommendations-articles"></a>

All 365Simple recommendations are provided directly, and articles are written by SoftwareOne experts and backed by data-driven intelligence.

### 365Simple Support tickets <a href="#help-and-support-overview" id="help-and-support-overview"></a>

This section provides a quick overview of all requests and incidents reported in the past 90 days including their respective status. Clicking on the widget takes you to the **Help and Support** page.

### Top 5 subscription changes <a href="#recent-subscription-changes" id="recent-subscription-changes"></a>

This widget provides a quick overview of all subscription changes in the current month, ordered by the biggest license seat count change. If no changes are available, the widget will provide access to the **My Subscriptions** page.

### Recent news from Microsoft <a href="#recent-news-from-microsoft" id="recent-news-from-microsoft"></a>

365Simple customers can also quickly check the latest Microsoft 365 news without leaving the platform. You can narrow down new features by products that are already rolled out, products that are planned, and products that are currently in development.

## Data refresh rate <a href="#data-refresh-rate" id="data-refresh-rate"></a>

As 365Simple surfaces data from multiple platform systems, there may be a difference in data refresh rate across the widgets. The table describes each widget and its data refresh rate.

| Section                         | Refresh rate                    |
| ------------------------------- | ------------------------------- |
| Billing                         | latest with every page refresh  |
| Recommendations                 | once a day                      |
| Product Usage                   | once a day                      |
| Top 5 Subscriptions by Assigned | once a day                      |
| Support tickets                 | every hour (after page refresh) |
| Service Articles                | latest with every page refresh  |
| Service Review                  | latest with every page refresh  |
