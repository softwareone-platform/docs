---
description: >-
  Define cloud budgets and assign them to groups within your business or cloud
  service provider.
---

# Working with budgets

Budgets are a part of Spend Management. Budgets allow you to assign individual budgets in two areas:

* **Customer-Centric Budgeting**: This area of Budgets allows you to assign individual Budgets to Custom Groups defined within Custom Groups (CG). This allows you to manage time periods and monetary values for your Spend defined by your business.
* **Service Provider Centric Budgeting**: This area of Budgets allows you to assign individual budgets to Enrollments, Subscriptions, or Tenants (depending on the provider terms). This allows you to manage time periods and monetary values for your spend tied to your providers.

***

### Before creating budgets <a href="#before-you-start" id="before-you-start"></a>

* **Set up a customer-centric view**. In order to assign budgets to individual groups, it is required to set up the structure in Custom Groups first. Without the setup of Custom Groups, you will only be able to see the “Per Provider” view in Budget Manager.
* **Set up a currency**. This is required to allow you to use your internal reporting currency across all Custom Groups, and manage the budgets and consumption in your individual currency. This is done for the following reasons:
  * If you are using multiple Providers in different sourcing currencies, PyraCloud will convert them to your set currency to harmonize the use for your convenience
  * The configured currency is also the default currency within Consumption Overview (native sourcing currency available at any time)
  * Consumption values are converted on a daily basis based on the Foreign Exchange rates

{% hint style="info" %}
**NOTE**: The currency can only be changed before configuring the first Budget. Changing currencies later will require the removal of all Budgets.
{% endhint %}

* **Currency in the Per Provider View**: The “Per Provider” view is always shown in the native sourcing currency and allows you to prepare your engagement with the Provider. Amounts and utilization are not converted and are available at any time within Budgets or for further reporting through Consumption Overview.

***

### Accessing budgets <a href="#accessing-budgets" id="accessing-budgets"></a>

**To access budgets**

* From the main menu, navigate to **Analyze** and select **Budgets**.

If you are the first user to use Budgets within your organization, you will find an empty Budget page with the request to set up the first reporting period.

***

### Custom group budgets <a href="#custom-group-budgets" id="custom-group-budgets"></a>

#### Creating Reporting Periods <a href="#creating-reporting-periods" id="creating-reporting-periods"></a>

Reporting Periods represent time periods that you use to schedule budgets in your organization. These can be for example: financial year, calendar year, quarters, or any custom time period.

Each Reporting Period is treated as an overall budget for all Custom Groups. Thus it carries information like Budget Amount or Budget Owner.

When creating the first Reporting Period, you will be asked to select a currency that will be applied to every Custom Group budget.

#### Creating Custom Group Budgets <a href="#creating-custom-group-budgets" id="creating-custom-group-budgets"></a>

Once you have adjusted your currency, the next step is to actually define the budgets. You can assign a budget to any custom group defined earlier within the Custom Groups (CG). The tree is available when you select **+ Add Budget**.

This will take you to the budget creation page:

You must provide the following information to create a budget:

* **Total Amount:** Value that you have budgeted to spend on this group
* **Owner Email Address**: Address of the person who owns the budget and will receive utilization notifications

Save the new budget to see it on the list.

#### Creating Child Budgets <a href="#creating-child-budgets" id="creating-child-budgets"></a>

You can create child budgets by selecting a child group. The child budget amount must be less or equal to the budget amount that is available for allocation in the parent budget.

#### Budget Details <a href="#budget-details" id="budget-details"></a>

Select **View** in the budget list of your selected budget to view more details.

The following details are displayed:

* **Current Budget Spend:** Spend generated by resources assigned to the budget group within the budget time period
* **Predicted Spend**: Prediction calculated until the end of the budget period
* **Budget Time Remaining**: Days left until the end of the budget period
* **Budget Time Period**: Start and end date of the budget
* **Budget Owner**: Email address of the person responsible for this budget
* **Budget Utilization Chart**: Monthly budget amount compared to monthly consumption

**Monthly Budget Breakdown**

By default, the budget amount will be equally distributed across budget months. Based on that, the table will provide you with consumption and utilization information for every month.

You can edit the monthly budgets to adjust the budget amount for every month.

**Child Budgets**

This tab provides information about child budget amounts and utilization. Consumption in child budgets is included in the parent budget utilization value.

<figure><img src="../../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

You can edit the child budget amounts by selecting **Edit Budgets.**

**Top 50 Resources**

This tab shows the top-consuming resources of the displayed budget. You can expand a resource to view more details.

* Select **View in Resource Manager** to open resource details in Resource Manager.
* Select **View Consumption** to open resource spend analytics.

<figure><img src="../../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

***

### Per Provider budgets <a href="#per-provider-budgets" id="per-provider-budgets"></a>

Select the **Per Provider** tab to open and manage budgets for your accounts.

<figure><img src="../../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

#### Creating Per Provider budgets <a href="#creating-per-provider-budgets" id="creating-per-provider-budgets"></a>

Select the **Add Budget** action to create a new budget. Depending on the Provider, the budget can be created for an Account and a Subscription.

<figure><img src="../../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

You will be taken to the new budget creation form. Provide the budget amount and email address of the person responsible for creating the budget.

<figure><img src="../../../.gitbook/assets/image (107).png" alt="" width="508"><figcaption></figcaption></figure>

If you create a budget for an Account – you will be asked to provide a budget name. In the case of subscription budgets, the name is automatically set to the subscription name.

{% hint style="info" %}
**NOTE**: There can be only one subscription budget created under an Account budget.
{% endhint %}

#### Budget details <a href="#budget-details-2" id="budget-details-2"></a>

To view more details, select a budget from the list and select **View.**

<figure><img src="../../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

The scope of the information is similar to the Custom Group Budget details page. If you are displaying Account budget details, the chart values are split by the account subscriptions.

**Subscriptions**

The list of subscriptions is provided in the “Subscriptions” tab with consumption and prediction details.

You can add and edit the budget for a selected subscription by clicking on “Edit Budgets” or “Add”.

**Top 50 Resources**

Click on the “Top 50 Resources” tab to see a list of the top resources consuming the most for that budget (Account or Subscription).

<figure><img src="../../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

You can expand the selected resource to view more details and navigate to the Resource page, or the Consumption Details page in Consumption Overview.

***

### Requesting budget creation and change <a href="#requesting-budget-creation-and-change" id="requesting-budget-creation-and-change"></a>

The list of budgets is displayed for you according to your Spend Management access configuration. It means you can have limited visibility to Custom Groups or Providers. Access rights are defined by your Site Administrator.

In the case of limited access, you cannot manage the budgets of the top-level Custom Groups (Custom Group view) or Subscriptions (Per Provider view). In this case, you will see the Budget request functionality.

#### Requesting a new budget <a href="#requesting-a-new-budget" id="requesting-a-new-budget"></a>

You will see the following option when you request a new Budget (available both for Custom Group and Per Provider Budgets):

<figure><img src="../../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

If you choose this option, the Budget Request form will be displayed:

Fill in the required Budget amount and confirm the request. The Budget Owner of the parent Custom Group will receive your request and will be able to create the Budget for you.

#### Requesting budget change <a href="#requesting-budget-change" id="requesting-budget-change"></a>

Similarly to new Budget requests, you can request for a change to be made to Budgets that you cannot modify yourself. Choose the “Request Budget Change” option to create your request:

<figure><img src="../../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

amountProvide the amount you request and submit your request. The Budget Owner of the parent Budget will receive your request.

***

### Budget creation and change notifications <a href="#budget-creation-and-change-notifications" id="budget-creation-and-change-notifications"></a>

When a budget is created or changed and the person performing that action is not the Budget Owner specified for the modified Budget, the Budget Owner receives a notification every time the following event occurs:

* A new budget is created.
* The budget amount has changed.
* The budget name has been changed.
* The start date or end date of the budget has been changed.
* The budget owner has been changed.

***

### Budget utilization alerts <a href="#budget-utilization-alerts" id="budget-utilization-alerts"></a>

Both Custom Group and the Per Provider Budgets offer utilization alerts.

You can set three thresholds that will trigger notifications for particular Budget Owners. These values are initially set by default, but you can adjust the percentage values by clicking on Edit as shown below:

<figure><img src="../../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**NOTE**: Alert settings are individual for Custom Group and Per Provider budgets.
{% endhint %}

Select **Manage Notifications** to edit notification settings in the Notification Hub Manager. You can select which notifications you want to receive (across all budgets) and how these notifications should be delivered.

***

### Cost models <a href="#cost-models" id="cost-models"></a>

If you have purchased any Reserved Instances, you can choose between two Cost Models:

* **Actual Cost**: Represents Reserved Instance purchase cost as a one-time cost (single spend record)
*   **Amortized Cost**: Equally distributes Reserved Instance purchase cost across months of the reservation time period

    <figure><img src="../../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>



Setting the Cost Model in Budgets will set the selected model as your default in other features (Consumption Overview and Chargeback Manager).