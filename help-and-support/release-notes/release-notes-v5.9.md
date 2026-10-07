---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: false
  actions:
    visible: true
  anchors:
    visible: true
tags:
  - tag: new
    primary: true
---

# Release notes v5.9

**Release Date: 7 October 2026**

Our latest release, Marketplace Platform v5.9, is here.&#x20;

To align with our monthly release cycle, Marketplace Platform now uses a new release numbering convention. Monthly releases will now be identified as v5.9, v5.10, and subsequent versions.

### Purchase Eligibility Validation

To provide a smoother purchasing experience, product eligibility is now validated as soon as you select **Buy Now** or **Buy More**.

If a product is unavailable for purchase, a message is displayed immediately with instructions to contact the Support team for assistance. This helps identify purchase restrictions at the start of the purchasing process rather than later during order creation.

### Terminate Multiple Subscriptions in a Single Request

You can now request termination for multiple subscriptions within the same agreement using a single request.&#x20;

This simplifies subscription management by allowing you to submit one order instead of creating separate orders for each subscription.

To create a multi-subscription termination order, open the agreement details page, select **Terminate** from the actions menu on the **Subscriptions** tab. Then, follow the guided workflow to submit the order. For more details, see [Terminate multiple subscriptions](../../modules-and-features/marketplace/subscriptions/terminate-multiple-subscriptions.md).

### Scheduled Renewal Orders

You can now schedule subscription changes to take effect on the renewal date by submitting a renewal order in advance.&#x20;

This allows you to plan renewal-related changes while keeping the current subscription unchanged until renewal.&#x20;

Scheduled renewal orders can be used for license quantity changes, plan upgrades or downgrades, and terminations. You can also track scheduled renewal orders and cancel them before the renewal date if your requirements change. For more details, see [Create and manage renewal orders](../../modules-and-features/marketplace/orders/create-and-manage-renewal-orders.md).

### New Suspend and Resume Order Types

Two new order types have been introduced to support subscription lifecycle management:

* **Suspend orders** temporarily pause active subscriptions while retaining the existing subscription configuration, data, and contractual terms.
* **Resume orders** reactivate suspended subscriptions and restore service access.

**Suspend** and **Resume** orders can only be created and managed by SoftwareOne. As a client, you can view these orders in Marketplace, but you cannot create or submit them.

### Configure Auto-Renewal for Multiple Subscriptions

You can now enable or disable auto-renewal for multiple subscriptions within the same agreement using a single configuration order.&#x20;

Previously, auto-renewal settings could only be changed for an individual subscription. This required a separate configuration order for each subscription.&#x20;

With this enhancement, you can create a configuration order from the agreement details page and apply the same auto-renewal action to multiple subscriptions at once. For more details, see [Configure auto-renewal for multiple subscriptions](../../modules-and-features/marketplace/subscriptions/configure-auto-renewal-for-multiple-subscriptions.md).

### Enhanced Credit Memo & Invoice Visibility

SoftwareOne Marketplace now displays credit memo information directly on invoices to help you identify invoices that have associated credit memos.&#x20;

You can now view associated credit memos directly from the invoice details page. The **Credit Memos** page also shows the original invoice for each credit memo. For more details, see [View credit memos associated with an invoice](../../modules-and-features/billing/invoices/view-credit-memos-associated-with-an-invoice.md).

### Microsoft CSP Extension Updates

New features and enhancements have been introduced for the SoftwareOne Marketplace CSP extension, including:

* Support for growth discounts on eligible CSP subscriptions.
* Ability to create bulk configuration and termination orders for CSP subscriptions.
* An enhanced subscription renewal workflow that simplifies choosing a renewal option.

For more details, see the [CSP extension release notes](../../extensions/microsoft-cloud-solution-provider/additional-resources/release-notes.md).
