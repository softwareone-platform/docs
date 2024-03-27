---
description: AzureSimple Dashboard.
---

# AzureSimple Dashboard

The AzureSimple dashboard provides an overview for clients using SoftwareOne’s AzureSimple service.  &#x20;

You can access the dashboard by navigating to the main menu of the Client Portal and selecting **Services >  AzureSimple**.

## Dashboard interface <a href="#selecting-your-tenant" id="selecting-your-tenant"></a>

The dashboard provides a single point of access to other areas of the platform, such as invoices and user administration. Through the dashboard, you can also view your saving opportunities, billing information, spike and outage alerts, and more.&#x20;

<figure><img src="../../.gitbook/assets/image (13) (1) (1).png" alt=""><figcaption><p>AzureSimple dashboard</p></figcaption></figure>

The dashboard consists of the following sections:

* [Select Microsoft tenant](azuresimple-dashboard.md#select-microsoft-tenant)
* [Potential monthly savings](azuresimple-dashboard.md#monthly-potential-savings)
* [AzureSimple billing](azuresimple-dashboard.md#billing-information)
* [Alerts](azuresimple-dashboard.md#spike-outage-alerts)
* [Service recommendations articles](azuresimple-dashboard.md#service-recommendations-articles)
* [Support tickets](azuresimple-dashboard.md#help-and-support-overview)

### Select Microsoft Tenant

If you have multiple Microsoft tenants, you will see a dropdown option next to your tenant name on the AzureSimple dashboard, allowing you to switch between tenants.&#x20;

When you switch tenants, the widget values in the dashboard change accordingly. As tenants are permission-based, you may not see all available customer tenants.  Also, widgets like Invoices and Add users are based on permissions. If you can't view the sections, contact your administrator to check your permissions.

### Potential monthly savings <a href="#monthly-potential-savings" id="monthly-potential-savings"></a>

This section is a monthly representation of potential AzureSimple savings opportunities. Clicking the section opens the **Recommendations** page to view detailed filtering and other savings recommendations.

### AzureSimple billing <a href="#billing-information" id="billing-information"></a>

This section displays billing cycles from the past 90 days. It usually contains the last three billing cycles, but it might also contain four if the billing cycle spans two months. Clicking the section opens the **Consumption Report** page.

{% hint style="info" %}
The section displays the default CSP agreement if you have multiple CSP agreements. Switching between agreements is currently not supported.
{% endhint %}

### Alerts <a href="#spike-outage-alerts" id="spike-outage-alerts"></a>

This section displays the three latest and most severe alerts from the past 30 days. This allows you to address unusual spending and prevent further cost impact. Clicking the section opens the Notifications Hub to view all notifications.

### Service recommendations articles <a href="#service-recommendations-articles" id="service-recommendations-articles"></a>

All AzureSimple recommendations are provided directly and the articles are written by SoftwareOne experts and backed by data-driven intelligence.

### Support tickets <a href="#help-and-support-overview" id="help-and-support-overview"></a>

This section provides a quick overview of all requests and incidents reported in the past 90 days including their respective status. Clicking on the section opens the **Help and Support** page where you can view all ticket details.

## Data refresh rate <a href="#data-refresh-rate" id="data-refresh-rate"></a>

As AzureSimple surfaces data from multiple platform systems, there may be a difference in data refresh rate across sections. The following table describes the data refresh rate for each section:

| Section                   | Refresh rate                                                                                 |
| ------------------------- | -------------------------------------------------------------------------------------------- |
| Potential Monthly Savings | the source is MS Azure Advisor, so the data could change every hour (after the page refresh) |
| Billing                   | once a day                                                                                   |
| Alerts                    | once a day                                                                                   |
| Support tickets           | every hour (after page refresh)                                                              |
| Service Articles          | latest with every page refresh                                                               |
| Service Review            | latest with every page refresh                                                               |
