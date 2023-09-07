---
description: >-
  Define cloud budgets and assign them to groups within your business or cloud
  service provider.
---

# Budgets

***

Budgets are a part of Spend Management. Budgets allow you to assign individual budgets in two areas:

* **Customer-Centric Budgeting**: This area of Budgets allows you to assign individual Budgets to Custom Groups defined within Custom Groups (CG). This allows you to manage time periods and monetary values for your Spend defined by your business.
* **Service Provider Centric Budgeting**: This area of Budgets allows you to assign individual budgets to Enrollments, Subscriptions, or Tenants (depending on the provider terms). This allows you to manage time periods and monetary values for your spend tied to your providers.

***

### Before creating budgets <a href="#before-you-start" id="before-you-start"></a>

* **Set up a customer-centric view:** In order to assign budgets to individual groups, it is required to set up the structure in Custom Groups first. Without the setup of Custom Groups, you will only be able to see the “Per Provider” view in Budget Manager.
* **Set up a currency:** This is required to allow you to use your internal reporting currency across all Custom Groups, and manage the budgets and consumption in your individual currency. This is done for the following reasons:
  * If you are using multiple Providers in different sourcing currencies, PyraCloud will convert them to your set currency to harmonize the use for your convenience
  * The configured currency is also the default currency within Consumption Overview (native sourcing currency available at any time)
  * Consumption values are converted on a daily basis based on the Foreign Exchange rates

{% hint style="info" %}
**NOTE**: The currency can only be changed before configuring the first Budget. Changing currencies later will require the removal of all Budgets.
{% endhint %}

* **Currency in the Per Provider View**: The “Per Provider” view is always shown in the native sourcing currency and allows you to prepare your engagement with the Provider. Amounts and utilization are not converted and are available at any time within Budgets or for further reporting through Consumption Overview.
