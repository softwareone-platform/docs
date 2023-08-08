# Office 365 Spend Reports

### What is Office 365 Consumption in PyraCloud?   <a href="#what-is-office-365-consumption-in-pyracloud" id="what-is-office-365-consumption-in-pyracloud"></a>

Office 365 Consumption in PyraCloud provides users with detailed Office 365 spend analysis. The data is based on billing data fetched daily.

Users can access multiple analytic reports and browse consumption cost information in easy to use interactive charts. The analysis is extended by leveraging information from other PyraCloud modules. Users can analyze spend per Custom Group (see [Custom Groups](https://help.pyracloud.com/knowledge-base/setting-up-custom-groups/)) or per Budget (see [Budgets](https://help.pyracloud.com/knowledge-base/creating-cloud-budgets/)).

### How to Access Office 365 Consumption <a href="#how-to-access-office-365-consumption" id="how-to-access-office-365-consumption"></a>

Users can access Office 365 Consumption in PyraCloud by choosing the following menu item and selecting “SaaS Office365 Consumption Details” or “Office365 Billing Consumption Details (Preview)” report:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-7.png" alt="" height="709" width="950"><figcaption><p><strong>Figure 1 – Accessing Office 365 Consumption in PyraCloud</strong></p></figcaption></figure>

### Office 365 Consumption <a href="#office-365-consumption" id="office-365-consumption"></a>

You can visualize and analyze your Office 365 EA and Office 365Simple spend. Each Azure active directory user and subscription is treated like a **resource**. You can assign it to a custom group, add tags or split the quantity between different business units.

#### Understand the “SaaS Office365 Consumption Details” Report <a href="#understand-the-saas-office365-consumption-details-report" id="understand-the-saas-office365-consumption-details-report"></a>

The Office365 Consumption Details Report display either “Cost” or “Quantity” data.

The Cost data is always reporting the initial monthly cost at the first day of month and additional cost due to subscription updates on a day that it happened. Cost data is calculated in single currency

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-8-1024x660.png" alt="" height="660" width="1024"><figcaption><p><strong>Figure 2 – Monthly initial cost and subscription update cost</strong></p></figcaption></figure>

The Quantity data is showing maximum number of subscriptions by product subscription per month.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-9-1024x635.png" alt="" height="635" width="1024"><figcaption><p><strong>Figure 3 – Subscription Quantity</strong></p></figcaption></figure>

**Office 365Simple Multiple Agreements Tenant**

The Cost data for Office 365Simple Multiple Agreements Tenant uses the average price calculated in a single currency. The average price is calculated at the first day of the month and on every subscription update. To check the billing data per agreement, please use “Office365 Billing Consumption Details (Preview)” report or Cloud Subscriptions (see [Cloud Subscription Billing](https://help.pyracloud.com/knowledge-base/understanding-the-cloud-subscription-billing-page/))

**NOTE:** If there are multiple buying currencies for a single Office365 tenant – the cost is calculated using the default currency and the most up to date exchange rates are applied. The exchange rates are updated daily by SoftwareONE using an external public rates source.

**Office 365 EA Tenant**

The Cost data for Office 365 EA Tenant uses the average price set manually in the Price List (see [Price Lists](https://help.pyracloud.com/knowledge-base/cloud-provider-price-lists/)).

If the price for a subscription is not set, an information banner will be displayed.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-10-1024x494.png" alt="" height="494" width="1024"><figcaption><p><strong>Figure 4 – Missing prices information banner</strong></p></figcaption></figure>

The price in Price List Center is set for every subscription per month and average calculation has to be done manually. All missing prices are visible in the missing prices Tab. If historical Quantity data is available, Cost data will be recalculated starting from “Effective Date”.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-11.png" alt="" height="407" width="594"><figcaption><p><strong>Figure 5 – Setting missing price</strong></p></figcaption></figure>

**Office 365 Tenant with Mixed Purchase Agreements**

The cost data for an Office 365 Tenant with mixed purchase agreements (i.e. Office 365Simple and EA) uses an average price calculation based on the **Office 365Simple prices** only.

We do not currently support setting custom prices for the subscriptions bought through Office 365 EA agreement. For Office 365 Tenants with mixed purchase agreements, an information banner will be displayed.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-12-1024x394.png" alt="" height="394" width="1024"><figcaption><p><strong>Figure 5 – Mixed Purchase Agreements Banner</strong></p></figcaption></figure>

#### Understand the Office 365 Resource Spend <a href="#understand-the-office-365-resource-spend" id="understand-the-office-365-resource-spend"></a>

Azure Active Directory users and subscriptions are treated like **resources**.

Azure Active Directory user **resource** cost, is a sum of costs of all subscriptions assigned to this user.

Subscription **resource** cost is a cost of all subscriptions that are not assigned to any Azure Active Directory user (Subscription **resource** has a name set to Subscription name and “Unassigned Pool” suffix).

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/image-13-1024x684.png" alt="" height="684" width="1024"><figcaption><p><strong>Figure 6 – Office 365 Resource Spend</strong></p></figcaption></figure>
