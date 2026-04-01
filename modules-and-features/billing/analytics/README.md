# Analytics

The **Analytics** page in the SoftwareOne Marketplace provides detailed insights into your billing data. It pulls the actual charges from your issued invoices to help you monitor spending, forecast budgets, and proactively manage your expenditure.

Analytics uses interactive charts and tables to help you understand your billed charges. It supports filtering and grouping options, allowing you to focus on the most relevant billed charges. You can select a specific time period, group data using predefined categories, and use filters to drill down and focus on the most relevant information.&#x20;

### Accessing billing analytics

To navigate to the **Analytics** page, select the main menu, then choose **Billing** > **Analytics**.&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Analytics.png" alt=""><figcaption><p>The Analytics page within SoftwareOne Marketplace.</p></figcaption></figure></div>

The **Analytics** page contains the following areas:

* **Filters sidebar** - The sidebar allows you to customize your view by selecting a time period and granularity (daily, monthly, or yearly). You can group data across various dimensions, such as **Agreement**, **Document type**, **Entitlement**, **Product**, and more, and narrow your results by selecting filters, operators, and currency. For details, see [Customize analytics with filters](customize-analytics-with-filters.md).
* **Analytics dashboard** - This section contains the **Export** option, which you can use to download the data in Excel format. For details, see [Export billing data](export-billing-data.md).
* **Analytics chart** - The chart area shows a visual representation of your billing data over time. It provides a visual breakdown of your billing data based on your selected filters and grouping. When you apply a **Group by** category (such as **Vendor** or **Product**), the chart automatically displays the top 10 entities with the highest billed amounts for that category. Any remaining entities outside of the top 10 are aggregated and displayed together as a single Others category, for example, "Others / Unmatched vendor profiles".
* **Analytics table** - The table displays your billing data in a structured format. The columns in the table update dynamically based on your chosen date granularity (for example, showing columns for 2023, 2024, 2025) and a **Total** column for quick reference.

{% hint style="info" %}
- When you first open the **Analytics** page, a **No chart details** message is displayed. You must apply the filters in the left sidebar and select **Show results** to view the data from your invoices and credit memos. For details, see [Customize analytics with filters](customize-analytics-with-filters.md).
- All data on the **Analytics** page is view-only. It cannot be edited.
{% endhint %}

### Currency selection and conversion <a href="#currency-selection-and-conversion" id="currency-selection-and-conversion"></a>

By default, **Analytics** displays all amounts in your standard billing currency. You can use the **Currency** filter in the filters sidebar to select a different target currency for financial reporting.

When you select a new target currency, the platform automatically applies the relevant exchange rates to convert your billing data. When a conversion has been applied, a note appears at the bottom of the data table stating: _"An exchange rate was applied for the selected currency."_

### Related topics

{% content-ref url="customize-analytics-with-filters.md" %}
[customize-analytics-with-filters.md](customize-analytics-with-filters.md)
{% endcontent-ref %}

{% content-ref url="export-billing-data.md" %}
[export-billing-data.md](export-billing-data.md)
{% endcontent-ref %}
