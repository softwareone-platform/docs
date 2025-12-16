# How to Split Billing Across Buyers

Split billing is a feature that allows you to divide the cost of a subscription across different buyers in your account. If your organization has multiple legal entities, split billing can be used to distribute costs effectively. To learn more, see [Split Billing](../../../modules-and-features/marketplace/billing/#split-billing).

In the Marketplace Platform, the split billing process begins by activating the feature from the user interface (UI), selecting buyers for allocation, and then specifying each buyer's allocation percentage or license count. This tutorial describes how to complete all of these steps.

In this tutorial, an agreement named _Adobe VIP Marketplace for Stark Industries_ contains three subscriptions. Currently, 100% of the billing for these subscriptions is assigned to a single buyer named _Stark Industries_. We'll activate split billing, add two new buyers named _Stark Industries II_ and _Stark Industries_ _III_, and then specify the allocation percentage for these buyers.

## Prerequisites

Before getting started with the tutorial, it's essential to have an understanding of the platform's [key concepts](../../platform-overview/key-concepts.md). You must also be familiar with the platform's interface and know how to navigate it.

## Splitting the billing across buyers

{% stepper %}
{% step %}
**Activating split billing**

Split billing can only be activated at the agreement level. To activate split billing:

1. Navigate to the **Agreements** page. Then, select the required agreement.&#x20;
2. On the agreement details page, select the arrow<img src="../../../.gitbook/assets/icon_down_arrow.png" alt="" data-size="line">choose **Split billing**.
3. In the **Split billing** dialog, select the checkbox to enable split billing, then select **Save**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/EnableSP (1).png" alt=""><figcaption><p>The option to enable split billing.</p></figcaption></figure></div>

Split billing is activated, and the **Split billing** tab appears on the agreement’s details page. You are now ready to configure the buyers to whom you want to allocate billing.&#x20;
{% endstep %}

{% step %}
**Configuring buyers**

In this tutorial, _Stark Industries_ is the **Owner** buyer who has been allocated 100% of the billing. We will configure _Stark Industries II_ and _Stark Industries III_ as additional buyers and then divide the costs across buyers.&#x20;

To configure buyers:

1. Select the **Split billing** tab on the agreement details page.
2. Select **Edit**.&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SplitBillingEdit (2).png" alt=""><figcaption><p>The Edit option on the Split billing tab.</p></figcaption></figure></div>

3. In the **Split billing** dialog, use the checkboxes to select buyers from the list of your active buyers. When done, select **Save**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SPBuyers (1).png" alt=""><figcaption><p>The list of buyers for billing allocation.</p></figcaption></figure></div>

_Stark Industries II_ and _Stark Industries III_ are added as buyers and displayed on the **Split billing** tab. You are now ready to allocate billing to these buyers.&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SPBuyers1 (1).png" alt=""><figcaption><p>The newly assigned buyers on the Split billing tab.</p></figcaption></figure></div>
{% endstep %}

{% step %}
**Allocating split billing**

Billing can be allocated by specifying percentages for each buyer. You can also specify the estimated license count. Both of these options are linked, meaning changing one updates the other automatically, although only the allocation % is used during billing (see [Split billing rules](../../../modules-and-features/marketplace/billing/#split-billing-rules) to learn more).

To start configuring the split for each buyer:

1. In the **Actions** column for the **Owner** buyer, select **Details**.
2. Find the required subscription and select **Edit**. The example agreement contains three subscriptions, but we will only configure allocation for the first subscription, called _Creative Cloud All Apps with Adobe Stock_.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SplitBillingSubscription (1).png" alt=""><figcaption><p>The Edit option for the subscription.</p></figcaption></figure></div>

3. Under **Allocation%**, enter the allocation percentage for each buyer. Then, select **Save**. In this example, 50% of the billing is allocated to _Stark Industries_ (owner buyer) and the remaining 50% to _Stark Industries II_. No split billing percentage is assigned to _Stark Industries III._&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/EditAllocation (1).png" alt=""><figcaption><p>The option to allocate percentages for buyers.</p></figcaption></figure></div>

4. The allocation is updated and displayed on the **Split billing details** page. By default, the allocation for the owner buyer is displayed:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Allocation (1).png" alt=""><figcaption><p>The split billing details page.</p></figcaption></figure></div>

Use the Buyer menu at the top to view the allocation for the other buyers (_Stark Industries II_ in this example):&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SPBuyers2 (1).png" alt=""><figcaption><p>The option to switch betwen buyers.</p></figcaption></figure></div>

5. Select **Close**. You'll be returned to the **Split billing details** tab.
{% endstep %}
{% endstepper %}

## Next steps

If you have additional subscriptions and want to split the billing, you can repeat the same steps for those subscriptions. You can also edit the split at any time. For instructions, see [Edit Split Billing](../../../modules-and-features/marketplace/billing/split-billing/edit-split-billing.md).
