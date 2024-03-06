---
description: Create a custom group budget.
---

# Create Custom Group budgets

## Before you begin <a href="#before-you-start" id="before-you-start"></a>

{% hint style="info" %}
Before creating budgets, note the following prerequisites:

* **Setup the customer-centric view** - To assign budgets to individual groups, you must first set up the structure in Custom Groups. Without Custom Groups, you can only see the **Per Provider** view in Budgets.
* **Setup a currency** - Currency setup is required so you can use your internal reporting currency across all Custom Groups, and manage the budgets and consumption in your currency. This is done for the following reasons:
  * If you are using multiple providers in different sourcing currencies, the platform will convert them to your set currency.
  * The configured currency is also the default currency within Consumption Overview (native sourcing currency available at any time).
  * Consumption values are converted daily based on the Foreign Exchange rates. A currency can only be changed before configuring the first budget. Changing currencies later will require the removal of all budgets.
{% endhint %}

## Create a Custom Group budget <a href="#creating-custom-group-budgets" id="creating-custom-group-budgets"></a>

You can assign a budget to any custom group defined within the Custom Groups. Follow these steps to create a budget:

1. From the main menu of the Client Portal, navigate to **Analyze** > **Budgets**.
2. On the **Budgets - Custom Groups** page, click **Add Budget**.

<figure><img src="../../.gitbook/assets/image (6).png" alt="" width="563"><figcaption><p>Budgets - Custom Groups</p></figcaption></figure>

3. (Optional) Use the **Search** option to find a specific group.
4. Select the custom group and click **Add**.&#x20;
5. On the **Budget Details** page, provide the following details:&#x20;
   * **Total Amount** - The amount that you have budgeted to spend on this group.
   * **Owner Email Address** - The email address of the person who owns the budget and will receive utilization notifications.
6. Click **Save**.

## Related topics

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

{% content-ref url="create-a-reporting-period.md" %}
[create-a-reporting-period.md](create-a-reporting-period.md)
{% endcontent-ref %}

{% content-ref url="create-per-provider-budgets.md" %}
[create-per-provider-budgets.md](create-per-provider-budgets.md)
{% endcontent-ref %}

{% content-ref url="view-budgets.md" %}
[view-budgets.md](view-budgets.md)
{% endcontent-ref %}

{% content-ref url="request-to-create-or-update-budgets.md" %}
[request-to-create-or-update-budgets.md](request-to-create-or-update-budgets.md)
{% endcontent-ref %}

{% content-ref url="edit-budget-utilization-alerts.md" %}
[edit-budget-utilization-alerts.md](edit-budget-utilization-alerts.md)
{% endcontent-ref %}
