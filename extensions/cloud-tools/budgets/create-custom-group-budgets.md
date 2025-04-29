---
description: Create a custom group budget.
---

# Create Custom Group Budgets

Before creating budgets, note the following prerequisites:

* To assign budgets to individual groups, you must first set up the structure in Custom Groups. Without Custom Groups, you can only see the **Per Provider** view in Budgets.
* Currency setup is also required so you can use your internal reporting currency across all Custom Groups, and manage the budgets and consumption in your currency. This is done for the following reasons:
  * If you are using multiple providers in different sourcing currencies, the platform will convert them to your set currency.
  * The configured currency is also the default currency within Consumption Overview (native sourcing currency available at any time).
  * Consumption values are converted daily based on the Foreign Exchange rates. A currency can only be changed before configuring the first budget. Changing currencies later will require the removal of all budgets.

## Create a Custom Group budget <a href="#creating-custom-group-budgets" id="creating-custom-group-budgets"></a>

You can assign a budget to any custom group defined within the Custom Groups. To create a budget:

1. Navigate to **Cloud tools** > **Budgets**.
2. On the **Budgets - Custom Groups** page, select **Add Budget**.

<figure><img src="../../../.gitbook/assets/image (867).png" alt="" width="563"><figcaption><p>Budgets - Custom Groups</p></figcaption></figure>

3. (Optional) Use the **Search** option to find a specific group.
4. Select the custom group and select **Add**.&#x20;
5. On the **Budget Details** page, provide the following details:&#x20;
   * **Total Amount** - The amount you have budgeted to spend on this group.
   * **Owner Email Address** - The email address of the person who owns the budget and will receive utilization notifications.
6. Select  **Save**.
