# Analytics

The **Analytics** feature gives you insight into billing data from your invoices.

Use this feature to monitor spending, forecast budgets, and manage costs.

Analytics also uses interactive charts and tables to help you analyze billed charges. You can choose a time period, group data by category, and apply filters to focus on the charges that matter most.

### Accessing billing analytics

To access **Analytics**, select the main menu, then choose **Billing** > **Analytics**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Analytics.png" alt=""><figcaption><p>The Analytics page within SoftwareOne Marketplace.</p></figcaption></figure></div>

### Analytics page layout

The page has four main areas:

* **Filters sidebar** - Customize your view by selecting a time period and granularity. Group data by dimensions such as **Agreement**, **Document type**, **Entitlement**, or **Product**. You can also apply filters, operators, and a currency. For more details, see [Customize analytics with filters](customize-analytics-with-filters.md).
* **Analytics dashboard** - Contains the **Export** option to download the current data. For more details, see [Export billing data](export-billing-data.md).
* **Analytics chart** - Shows billed charges over time based on your selected filters and grouping. When you apply a **Group by** category, the chart displays the top 10 entities with the highest billed amounts. Remaining entities are grouped into a single Others category, such as "Others / Unmatched vendor profiles".
* **Analytics table** - Displays billing data in a structured format. The columns update based on your chosen date granularity and include a **Total** column for quick reference.

{% hint style="info" %}
- When you first open **Analytics**, no chart data appears. Apply filters in the left sidebar, then select **Show results** to view data from your invoices and credit memos. For more details, see [Customize analytics with filters](customize-analytics-with-filters.md).
- All data on the **Analytics** page is view-only. You cannot edit it.
{% endhint %}

### Currency selection and conversion <a href="#currency-selection-and-conversion" id="currency-selection-and-conversion"></a>

By default, **Analytics** shows amounts in your standard billing currency. Use the **Currency** filter in the sidebar to select a different target currency.

When you select a new target currency, the platform automatically applies the relevant exchange rates to convert your billing data.

When a conversion is applied, a note appears at the bottom of the data table stating: _"An exchange rate was applied for the selected currency."_

### Related topics

{% content-ref url="customize-analytics-with-filters.md" %}
[customize-analytics-with-filters.md](customize-analytics-with-filters.md)
{% endcontent-ref %}

{% content-ref url="export-billing-data.md" %}
[export-billing-data.md](export-billing-data.md)
{% endcontent-ref %}
