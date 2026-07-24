---
description: >-
  Learn how coterminosity aligns subscription renewal dates and the rules that
  apply in Marketplace Platform.
---

# Subscription coterminosity

Subscription coterminosity (renewal alignment) allows multiple Microsoft subscriptions within an agreement to share the same renewal date.&#x20;

When coterminosity is enabled, new eligible subscriptions are aligned to an existing subscription end date instead of receiving their own independent renewal date. This helps simplify subscription management, billing, and renewals.

Benefits of subscription coterminosity include:

* **Add-on alignment** – Terminate or renew add-on subscriptions together with the existing subscription.&#x20;
* **Align subscription renewals with the fiscal year** – Align subscription renewals with your organization's fiscal year.
* **Consistent invoicing** – Simplify billing by aligning subscriptions to a consistent renewal schedule.&#x20;
* **Flexibility renewal dates** – Different groups of subscriptions can use different coterminous dates.

### Conditions for coterming subscriptions <a href="#conditions-for-aligning-subscriptions-using-coterminosity" id="conditions-for-aligning-subscriptions-using-coterminosity"></a>

In Marketplace Platform, the following rules apply:

* Only license-based Microsoft NCE subscriptions support coterminosity.&#x20;
* Azure, Perpetual Software, and Software subscriptions don't support coterminosity.
* Annual and triannual term subscriptions can't be coterminated with monthly subscriptions.
* Add-on subscriptions can be aligned to existing subscription end dates only if they belong to the same partner.
* Yearly subscriptions can't be aligned with monthly subscriptions. If coterming is enabled using a monthly date and an annual subscription is ordered, a warning is displayed stating that the end date must be updated. Otherwise, the subscription is created without coterminosity. See [Subscription End Date Errors](subscription-end-date-errors.md) for details.

#### Example

The following example shows how coterminosity works.

An agreement is created on 14 March 2025 with an annual subscription. On 25 April 2025, a second annual subscription is added to the same agreement.

* Without coterminosity, the second subscription renews on 25 April 2026. The monthly date will be 24 May 2025.
* With coterminosity, the subscription renews on 15 March 2026, aligning its renewal date with the existing subscription in the agreement. The monthly date will be 15 May 2025.

<table data-header-hidden><thead><tr><th width="337"></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Subscription term</strong></td><td>Annual</td><td>Monthly</td></tr><tr><td><strong>Renewal date without coterminosity</strong></td><td>25 April 2026</td><td>24 May 2025</td></tr><tr><td><strong>Renewal date with coterminosity</strong></td><td>15 March 2026</td><td>15 May 2025</td></tr></tbody></table>
