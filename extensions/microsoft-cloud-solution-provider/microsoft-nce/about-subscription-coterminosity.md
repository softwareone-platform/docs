# About Subscription Coterminosity

Coterming refers to aligning the renewal dates for multiple Microsoft subscriptions under a single agreement. Microsoft allows coterming of new subscriptions immediately when they are created.

Coterming is used in enterprise-level contracts or licensing agreements, where various Microsoft products are purchased separately but have the same expiration or renewal date. By making the dates coterminous, organizations can streamline license management, simplify billing, and eliminate the need to track separate renewal dates for each product. Additionally, this approach enables companies to renew all their Microsoft services at once, thus saving time and reducing the administrative burden.

The following are the benefits of aligning your subscription term end dates:

* **Add-on management** - You can terminate or renew an add-on subscription at the same time as the existing subscription.&#x20;
* **Align subscription renewals with the fiscal year** - A subscription's renewal dates can be aligned with the fiscal year's start date so that the budget can be allocated accordingly each year.
* **Consistent and efficient invoicing** - All subscriptions align to a consistent invoicing experience, simplifying the billing process. The billing period and charge cycle for both consumption-based and license-based subscriptions follow a standard calendar-month cycle. This means you don't have to worry about buying subscriptions on different dates. The charge cycle aligns with the calendar month, and we'll prorate the cost for you to bill your customers.
* **Flexibility for end dates** - Each group of subscriptions can have their coterminous date.

## Conditions for coterming subscriptions <a href="#conditions-for-aligning-subscriptions-using-coterminosity" id="conditions-for-aligning-subscriptions-using-coterminosity"></a>

Coterminosity allows you to align the end date of a new subscription with that of an existing subscription. In the Marketplace Platform, the following coterming rules apply to subscriptions:&#x20;

* Aligning end dates is only possible for license-based NCE subscriptions. Azure, Perpetual Software, and Software subscriptions do not support aligning the end dates.
* Annual and triannual term subscriptions cannot be coterminated with a monthly term subscription.
* You can coterminate your add-on subscriptions to existing subscription end dates as long as they belong to the same partner.
* Yearly subscriptions cannot be aligned with monthly subscriptions. If coterming is enabled with a monthly date and an annual subscription is ordered, a message is displayed stating that the end date will require updating; otherwise, the subscription will be created without coterminosity. See [Subscription End Date Errors](subscription-end-date-errors.md) for details.

#### Example

The following example shows how coterminosity works in the platform:

On 14 March 2025, a new agreement is created with an annual subscription. Then, a change order is created within the same agreement on 25 April 2025 for a new subscription.

* Without coterming, the annual date of the subscription renewal will be 25 April 2026, and the monthly date will be 24 May 2025.
* With coterming, the annual subscription renewal will be 15 March 2026, and the monthly date will be 15 May 2025.

| **Subscription term**           | Annual        | Monthly     |
| ------------------------------- | ------------- | ----------- |
| **Renewal date without coterm** | 25 April 2026 | 24 May 2025 |
| **Renewal date with coterm**    | 15 March 2026 | 15 May 2025 |
