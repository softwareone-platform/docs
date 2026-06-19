---
description: Learn how to choose a currency for your Marketplace invoices.
---

# How to set or change billing currency

This tutorial describes how to choose the billing currency for a Marketplace agreement.

SoftwareOne issues invoices at the agreement level. It means that invoices are generated for specific agreements. Therefore, currency selection must be done at the agreement level.

There are two ways to choose a billing currency. You can select it when creating a new agreement. Alternatively, you can change it after the order is placed.

{% hint style="info" %}
* If your billing currency differs from your base currency, invoice amounts use the exchange rate in effect when the invoice is generated.
* If you don't see the option to change the currency, it means the seller doesn't offer additional billing currencies.
{% endhint %}

### Set currency for a new agreement

{% stepper %}
{% step %}
**Start a new purchase**

1. Go to **Catalog** > **Products**.
2. Select the product you want, then select **Buy now**. The purchase flow starts.
3. Under **Select agreement**, select **Create agreement**.
4. Continue through the steps until you reach the **Billing currency** step.
{% endstep %}

{% step %}
**Choose the billing currency**

1. From the **Billing currency** list, select your preferred currency for future invoices.
2. Select **Next**.
3. Complete the remaining steps to finalize your order.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/billing-currency-purchase-wizard.png" alt="Purchase wizard showing the Billing currency step for a new agreement"><figcaption><p>Select the billing currency for the new agreement.</p></figcaption></figure></div>
{% endstep %}
{% endstepper %}

### Change currency for an existing agreement

Changing the billing currency affects future invoices only. Past invoices remain in the original currency.

{% stepper %}
{% step %}
**Open the agreement**

1. Go to **Marketplace** > **Agreements**.
2. Select the agreement whose currency you want to update.
3. On the agreement details page, select the dropdown arrow <i class="fa-chevron-down">:chevron-down:</i>, then choose **Billing currency**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/billing-currency-agreement.png" alt="Agreement details page menu with the Billing currency option"><figcaption><p>Open the menu, then select <strong>Billing currency</strong>.</p></figcaption></figure></div>
{% endstep %}

{% step %}
**Save the new currency**

1. In the **Select billing currency** dialog, choose the new currency.
2. Select **Save**.
{% endstep %}
{% endstepper %}

### Next steps

Future Marketplace invoices are issued in your selected billing currency. You can view and manage invoices using the [Invoices](../../../modules-and-features/marketplace/billing/invoices/) page.
