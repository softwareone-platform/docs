---
description: Divide subscription costs across buyers in your account.
---

# How to split billing across buyers

Split billing is a feature that allows you to divide the cost of a subscription across different buyers in your account. If your organization has multiple legal entities, split billing can be used to distribute costs effectively. To learn more, see [Split Billing](../../../modules-and-features/marketplace/billing/#split-billing).

In the SoftwareOne Marketplace, the split billing process begins by activating the feature from the user interface (UI), selecting buyers for allocation, and then specifying each buyer's allocation percentage or license count. This tutorial describes how to complete all of these steps.

In this tutorial, an agreement named _Adobe VIP Marketplace for Stark Industries_ contains three subscriptions. Currently, 100% of the billing for these subscriptions is assigned to a single buyer named _Stark Industries_. We'll activate split billing, add two new buyers named _Stark Industries II_ and _Stark Industries_ _III_, and specify the allocation percentage for these buyers.

### Split billing across buyers

{% stepper %}
{% step %}
**Activate split billing**

Split billing can only be activated at the agreement level. To activate split billing:

1. Open the **Agreements** page and select the required agreement.
2. On the agreement details page, select the dropdown arrow <i class="fa-chevron-down">:chevron-down:</i>, then choose **Split billing**.
3. Select the checkbox, then select **Save**. &#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/EnableSP (1).png" alt=""><figcaption><p>Select the checkbox to enable split billing.</p></figcaption></figure></div>

Split billing is activated, and the **Split billing** tab appears on the agreement details page.&#x20;
{% endstep %}

{% step %}
**Configure buyers**

In this tutorial, _Stark Industries_ is the **Owner** buyer who has been allocated 100% of the billing. We will configure _Stark Industries II_ and _Stark Industries III_ as additional buyers and divide costs across buyers.&#x20;

To configure buyers:

1. On the agreement details page, select the **Split billing** tab.
2. Select **Edit**.&#x20;
3. In the **Split billing** dialog, select the required buyers, then select **Save**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SPBuyers (1).png" alt=""><figcaption><p>Choose buyers for allocating billing.</p></figcaption></figure></div>

_Stark Industries II_ and _Stark Industries III_ are added as buyers and displayed on the **Split billing** tab. You are now ready to allocate billing to these buyers.&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SPBuyers1 (1).png" alt=""><figcaption><p>The newly assigned buyers on the Split billing tab.</p></figcaption></figure></div>
{% endstep %}

{% step %}
**Allocate percentage**

Billing can be allocated by specifying percentages for each buyer. You can also specify the estimated license count. Both of these options are linked, meaning that changing one automatically updates the other, although only the allocation % is used during billing (see [Split billing rules](../../../modules-and-features/marketplace/billing/#split-billing-rules) to learn more).

To start configuring the split for each buyer:

1. In the **Actions** column for the **Owner** buyer, select **Details**.
2. Find the required subscription, then select **Edit**. The example agreement contains three subscriptions, but we will only configure allocation for the first subscription, called _Creative Cloud All Apps with Adobe Stock_.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SplitBillingSubscription (1).png" alt=""><figcaption><p>The Edit option for the subscription.</p></figcaption></figure></div>

3. Under **Allocation%**, enter the allocation percentage for each buyer. Then, select **Save**. In this example, 50% of the billing is allocated to _Stark Industries_ (owner buyer) and the remaining 50% to _Stark Industries II_. No split billing percentage is assigned to _Stark Industries III._&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/EditAllocation (1).png" alt=""><figcaption><p>The option to allocate percentages for buyers.</p></figcaption></figure></div>

4. The allocation is updated and displayed on the **Split billing details** page. By default, the allocation for the owner buyer is displayed:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/Allocation (1).png" alt=""><figcaption><p>The split billing details page.</p></figcaption></figure></div>

Use the Buyer menu at the top to view the allocation for the other buyers (_Stark Industries II_ in this example):&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/SPBuyers2 (1).png" alt=""><figcaption><p>The option to switch betwen buyers.</p></figcaption></figure></div>

5. Select **Close**. You are returned to the **Split billing details** tab.
{% endstep %}
{% endstepper %}

### Next steps

Repeat the same steps if you have additional subscriptions and want to split the billing for those subscriptions.&#x20;

You can also edit the split at any time. For details, see [Edit split billing](../../../modules-and-features/marketplace/billing/split-billing/edit-split-billing.md).
