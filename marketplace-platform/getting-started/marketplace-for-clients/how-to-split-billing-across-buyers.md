# How to Split Billing Across Buyers

Split billing is a feature that allows you to divide the cost of a subscription across different buyers in your account. If your organization has multiple legal entities, split billing can be used to distribute costs effectively. To learn more, see [Split Billing](../../../modules-and-features/marketplace/billing/#split-billing).

In the Marketplace Platform, the split billing process begins by activating the feature from the user interface (UI), selecting buyers for allocation, and then specifying each buyer's allocation percentage or license count. This tutorial describes how to complete all of these steps.

In this tutorial, an agreement named _Adobe VIP Marketplace for Stark Industries_ contains three subscriptions. Currently, 100% of the billing for these subscriptions is assigned to a single buyer named _Stark Industries_. We'll activate split billing, add two new buyers named _Stark Industries II_ and _Stark Industries_ _III_, and then specify the allocation percentage for these buyers.

## Prerequisites

Before getting started with the tutorial, it's essential to have an understanding of the platform's [key concepts](../key-concepts.md). You must also be familiar with the platform's interface and know how to navigate it.

## 1. Activating split billing

Split billing can only be activated at the agreement level. To activate split billing:

1. Navigate to the **Agreements** page and select the required agreement.&#x20;

<figure><img src="../../../.gitbook/assets/Agreements (5).png" alt=""><figcaption><p>Agreements page</p></figcaption></figure>

2. On the details page of the agreement, click the down arrow<img src="../../../.gitbook/assets/image (41).png" alt="" data-size="line"> in the upper right and select **Split billing**.

<figure><img src="../../../.gitbook/assets/SP (1).png" alt=""><figcaption><p>Details page of the ageement</p></figcaption></figure>

3. In the **Split billing** dialog, select the checkbox and then click **Save**.

<figure><img src="../../../.gitbook/assets/EnableSP (1).png" alt=""><figcaption><p>Enable split billing checkbox</p></figcaption></figure>

Split billing is activated and the **Split billing** tab appears on the agreement’s details page. You are now ready to configure buyers to allocate billing to.&#x20;

<figure><img src="../../../.gitbook/assets/SplitBillingTab (1).png" alt=""><figcaption><p>Split billing tab on the agreement details page</p></figcaption></figure>

## 2. Configuring buyers

In this tutorial, _Stark Industries_ is the **Owner** buyer who has been allocated 100% of the billing.&#x20;

We'll configure _Stark Industries II_ and _Stark Industries III_ as additional buyers and then divide the costs across buyers. To start configuring buyers:

1. On the **Split billing** tab, click **Edit**.&#x20;

<figure><img src="../../../.gitbook/assets/SplitBillingEdit (2).png" alt=""><figcaption><p>Edit option on the Split billing tab</p></figcaption></figure>

2. In the **Split billing** dialog, use the checkboxes to select the buyers from the list of your active buyers and then click **Save**.&#x20;

<figure><img src="../../../.gitbook/assets/SPBuyers (1).png" alt=""><figcaption><p>List of buyers</p></figcaption></figure>

_Stark Industries II_ and _Stark Industries III_ are added as buyers and displayed on the **Split billing** tab. You are now ready to allocate billing to these buyers.&#x20;

<figure><img src="../../../.gitbook/assets/SPBuyers1 (1).png" alt=""><figcaption><p>Newly assigned buyers on the Split billing tab</p></figcaption></figure>

## 3. Splitting the allocations

Billing can be allocated by specifying percentages for each buyer. You can also specify the estimated license count. Both of these options are linked, meaning changing one updates the other automatically, although only the allocation % is used during billing (see [Split billing rules](../../../modules-and-features/marketplace/billing/#split-billing-rules) to learn more).

To start configuring the split for each buyer:

1. In the **Actions** column for the **Owner** buyer, click **Details**.

<figure><img src="../../../.gitbook/assets/Details (3).png" alt=""><figcaption><p>Details option for the Owner buyer</p></figcaption></figure>

2. For the required subscription, click **Edit**.

This example agreement contains three subscriptions, but we'll only configure allocation for the first subscription, called _Creative Cloud All Apps with Adobe Stock_.

<figure><img src="../../../.gitbook/assets/SplitBillingSubscription (1).png" alt=""><figcaption><p>Edit option for the subscription</p></figcaption></figure>

3. In **Allocation %**, enter the allocation percentage for each buyer and click **Save**.&#x20;

In this example, 50% of the billing is allocated to _Stark Industries_ (owner buyer) and the remaining 50% to _Stark Industries II_. No percentage is assigned to _Stark Industries III._&#x20;

<figure><img src="../../../.gitbook/assets/EditAllocation (1).png" alt=""><figcaption><p>Allocate percentages for buyers</p></figcaption></figure>

4. The allocation is updated and displayed on the **Split billing details** page. By default, the allocation for the owner buyer is displayed:

<figure><img src="../../../.gitbook/assets/Allocation (1).png" alt=""><figcaption><p>Split billing details page</p></figcaption></figure>

Use the Buyer menu at the top to view the allocation for the other buyers (_Stark Industries II_ in this example):&#x20;

<figure><img src="../../../.gitbook/assets/SPBuyers2 (1).png" alt=""><figcaption><p>Buyer menu</p></figcaption></figure>

5. Click **Close**. You'll be returned to the **Split billing details** tab.

<figure><img src="../../../.gitbook/assets/SPBuyers3 (1).png" alt=""><figcaption><p>Close option</p></figcaption></figure>

## Next steps

If you have additional subscriptions and want to split the billing, you can repeat the same steps for those subscriptions. You can also edit the split at any time. For instructions, see [Edit Split Billing](../../../modules-and-features/marketplace/billing/billing/edit-split-billing.md).
