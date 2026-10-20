---
description: Find common error messages and how to resolve them.
---

# Common error messages

You can find the error messages you might see when you order, change, renew, or return Adobe licenses, and how to resolve them. This helps you fix the problem and place your order again.

Messages are grouped by the task you were doing. Parts of a message in angle brackets, such as `<field>`, are replaced with your own details. Some error codes are used for more than one message, so look for the message text rather than the code.

### Setting up an account or placing an order

<details>

<summary>"The provided &#x3C;field> length must be between 4 and 59 characters." (VIPM0008)</summary>

**Cause** – The company name is too short or too long.

**Resolution** – Enter a company name of 4 to 59 characters, then place the order again.

</details>

<details>

<summary>"The provided &#x3C;field> must only contain letters, digits, spaces, commas, periods, ampersands, hyphens, apostrophes, parentheses, forward slashes, backslashes, double quotes, and underscores." (VIPM0009)</summary>

**Cause** – The company name contains a character that Adobe does not accept.

**Resolution** – Remove the character, then place the order again.

</details>

<details>

<summary>"The &#x3C;field> contains invalid components: &#x3C;details>." (VIPM0010, VIPM0011)</summary>

**Cause** – Part of the company address or the contact details is missing, invalid, or too long. The message lists the parts to fix.

**Resolution** – Correct the listed parts, then place the order again. The following table describes the maximum lengths:

| Field                             | Maximum length |
| --------------------------------- | -------------- |
| Address line 1 and Address line 2 | 60 characters  |
| City                              | 40 characters  |
| ZIP/Postal code                   | 40 characters  |
| Phone number                      | 40 characters  |
| First name and Last name          | 35 characters  |

</details>

<details>

<summary>"The &#x3C;field> is not valid: &#x3C;details>." (VIPM0001, VIPM0003, VIPM0004)</summary>

**Cause** – Adobe rejected the company name, address, or contact when it tried to create your account. The order is paused in **Querying** status.

**Resolution** – Open the order, correct the field named in the message, and select **Process**. Do this before the order's processing deadline, or the order fails.

</details>

<details>

<summary>"The order cannot contain multiple lines for the same item: &#x3C;items>." (VIPM0016)</summary>

**Cause** – The same item appears on more than one line of the order.

**Resolution** – Combine the quantities on one line, then place the order again.

</details>

<details>

<summary>"The order cannot contain new lines for an existing item: &#x3C;items>." (VIPM0017)</summary>

**Cause** – You added a new line for an item you already have on the agreement.

**Resolution** – Change the quantity of the existing subscription instead. For more details, see [Increase Adobe license quantity](manage-subscriptions/increase-adobe-license-quantity.md).

</details>

<details>

<summary>"The agreement is not eligible for market segment &#x3C;segment>." (VIPM0024)</summary>

**Cause** – Adobe has not confirmed that your organization is eligible for the Education or Government segment.

**Resolution** – Contact SoftwareOne to confirm your eligibility.

</details>

<details>

<summary>"Due date &#x3C;date> for order processing is reached." (VIPM0025)</summary>

**Cause** – The order was still in **Processing** or **Querying** status when its processing deadline passed, so it failed.

**Resolution** – Place the order again. If it was waiting in **Querying** status, complete the action the order asks for before you select **Process**.

</details>

### 3-year commitments

<details>

<summary>"The &#x3C;field> must be an integer number equal to 10 or greater." (VIPM0013)</summary>

**Cause** – The minimum number of licenses for a 3-year commitment is less than 10.

**Resolution** – Enter 10 or more, then place the order again.

</details>

<details>

<summary>"The &#x3C;field> must be an integer number equal to 1000 or greater." (VIPM0014)</summary>

**Cause** – The minimum number of consumables for a 3-year commitment is less than 1000.

**Resolution** – Enter 1000 or more, then place the order again.

</details>

<details>

<summary>"To request 3-year commitment benefits you must fill at least one parameter between …" (VIPM0015)</summary>

**Cause** – You asked for a 3-year commitment but didn't enter a minimum number of licenses or consumables.

**Resolution** – Enter at least one of the two minimums, then place the order again.

</details>

<details>

<summary>"The quantity selected of &#x3C;quantity> would place the account below the minimum commitment of &#x3C;minimum> licenses for the three-year commitment." (VIPM0034)</summary>

**Cause** – The order would take your licenses below the minimum you committed to. The same message can refer to consumables.

**Resolution** – Change the quantities so you stay at or above your minimum. If you need to go below it, contact SoftwareOne.

</details>

<details>

<summary>"The order has failed. The reduction in quantity would place the account below the minimum commitment of …" (VIPM0020)</summary>

**Cause** – The reduction would take your licenses or consumables below your 3-year commitment minimum.

**Resolution** – Reduce by a smaller quantity, so you stay at or above your minimum. If you need to go below it, contact SoftwareOne.

</details>

<details>

<summary>"The 3-year commitment is in status &#x3C;status>. Please contact support to renew the commitment." (VIPM0035)</summary>

**Cause** – Your 3-year commitment has expired, was declined, or is no longer compliant with its minimums.

**Resolution** – Contact SoftwareOne.

</details>

### Reducing, returning, and terminating licenses

<details>

<summary>"Cannot return the entire quantity of all subscriptions in this order. Consider disabling auto-renewal for these subscriptions instead using a Configuration Order." (VIPM0033)</summary>

**Cause** – You placed a termination order for a subscription, or an agreement, where at least one license is outside the 14-day return window, so not every license can be returned.

**Resolution** – To stop the subscription at your anniversary date, turn off auto-renewal with a configuration order. For more details, see [Change Adobe subscription auto-renewal](manage-subscriptions/change-adobe-subscription-auto-renewal.md). To return the licenses that are still returnable, reduce the subscription's quantity instead. For more details, see [Reduce Adobe license quantity](manage-subscriptions/reduce-adobe-license-quantity.md).

</details>

<details>

<summary>"Adobe rejected the return because it would reduce the three-year commitment below its minimum commit quantity: …" (VIPM0056)</summary>

**Cause** – You have a 3-year commitment, and the return would take your licenses below your committed minimum. Nothing was returned.

**Resolution** – Reduce by a smaller quantity, so you stay at or above your minimum. If you need to go below it, contact SoftwareOne.

</details>

<details>

<summary>"The downsize could not be completed after part of it was already returned to Adobe. Returned lines were not undone. …" (VIPM0055)</summary>

**Cause** – Adobe refused part of a reduction after other parts had already been returned. The message lists each product as `RETURNED`, `PARTIAL`, `NOT PROCESSED`, or `DEFERRED`.

**Resolution** – The returns already made stay in place and are credited. Check the subscription's **Current quantity** and **Renewal quantity**, then place a new change order for anything that still needs changing. Contact SoftwareOne if you need help.

</details>

For more details, see [Returns and termination](returns-and-termination/).

### Orders around your anniversary date and renewals

<details>

<summary>"Orders cannot be placed within 24 hours of the renewal date. Please wait until after the renewal date and make your required changes with Change, Configuration, or Termination Orders." (VIPM0034)</summary>

**Cause** – You placed a change, configuration, or termination order on the day before your anniversary date or on the anniversary date itself (US Pacific time).

**Resolution** – Wait until the day after your anniversary date, then place the order again. For more details, see [Key dates and deadlines](key-dates-and-deadlines.md).

</details>

<details>

<summary>"An early renewal has already been placed for this agreement, so Change, Configuration and Termination orders are locked until it takes effect at the anniversary date. Please re-open the renewal wizard to make renewal-affecting changes." (VIPM0051)</summary>

**Cause** – You renewed early, so other change, configuration, and termination orders are locked.

**Resolution** – Make renewal changes in the renewal wizard. Other changes are possible again after your anniversary date.

</details>

<details>

<summary>"A renewal has been staged for this agreement, so Change, Configuration and Termination orders are locked until it takes effect at the anniversary date. Please re-open the renewal wizard to make renewal-affecting changes." (VIPM0054)</summary>

**Cause** – A renewal plan for your anniversary date is in place, so other change, configuration, and termination orders are locked.

**Resolution** – Change the plan in the renewal wizard. Other changes are possible again after your anniversary date.

</details>

<details>

<summary>"This renewal plan was built for the &#x3C;date> renewal date, but the customer's renewal date is now &#x3C;date>, so nothing was changed. Please re-open the renewal wizard to plan the next renewal." (VIPM0057)</summary>

**Cause** – Your anniversary date moved after the renewal plan was made, so the plan was not applied.

**Resolution** – Open the renewal wizard and plan the renewal again.

</details>

<details>

<summary>"The previous renewal order &#x3C;order> of subscription &#x3C;subscription> was placed on &#x3C;date>, outside the 14-day return window, so it cannot be returned." (VIPM0053)</summary>

**Cause** – Your renewal removes a subscription that was renewed early more than 14 days ago, so that renewal cannot be returned.

**Resolution** – Keep the subscription in the renewal, or contact SoftwareOne.

</details>

<details>

<summary>"Adobe did not confirm the flexible discount code(s) …, so nothing was changed" or "… so nothing was renewed or invoiced" (VIPM0055, VIPM0056)</summary>

**Cause** – Adobe refused a discount code in your renewal, so the renewal was not placed and you were not charged.

**Resolution** – Open the renewal wizard, remove or change the discount code on the **Promotions** step, and place the renewal again.

</details>

<details>

<summary>"Only one flexible discount code per line item is allowed: …" (VIPM0052)</summary>

**Cause** – More than one discount code was applied to the same item.

**Resolution** – Keep one discount code for each item, then place the order again.

</details>

### Renewal wizard messages

The following table describes the messages you might see in the renewal wizard:

| Message                                                                                                                                                                                  | What to do                                                                                                                               |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| "You can plan your renewal from 30 days until 2 days before your renewal date. Meanwhile, you can still use Change, Configuration, and Termination orders to manage your subscriptions." | Come back when the renewal window opens. For more details, see [Key dates and deadlines](key-dates-and-deadlines.md).                    |
| "It's too late to plan this renewal. Renewals can be planned up to 2 days before your renewal date. Your subscriptions will renew as they're currently set up."                          | Your subscriptions renew with their current settings. You can make changes after your anniversary date.                                  |
| "Your renewal date is unknown, so this renewal cannot be planned right now. Your subscriptions will renew as they're currently set up."                                                  | Contact SoftwareOne.                                                                                                                     |
| "This agreement has no active subscriptions. You cannot plan a renewal for this agreement."                                                                                              | There is nothing to renew on this agreement.                                                                                             |
| "Orders can only be created for Active agreements. The agreement is currently \<status>."                                                                                                | Wait until the current order completes and the agreement is **Active** again.                                                            |
| "The renewal is available to client accounts only."                                                                                                                                      | Sign in with your client account.                                                                                                        |
| "Adobe handles a renewal and any additions as separate orders, so this order cannot include both. …"                                                                                     | Keep only the renewal lines or only the additions, as the message describes. Place the rest as a separate order.                         |
| "Renewing now cannot go above the quantity you hold. …"                                                                                                                                  | Renew the quantity you hold now. Add extra licenses in a separate order after the renewal is placed.                                     |
| "Subscription \<subscription> cannot renew fewer seats than the \<quantity> already early-renewed."                                                                                      | Keep at least the quantity you already renewed early. To return licenses, reduce the subscription with a change order after the renewal. |
| "The renewal plan would place the account below the minimum quantities committed for the three-year commitment."                                                                         | Increase the quantities so you stay at or above your 3-year commitment minimum.                                                          |
| "The renewal plan includes products that cannot renew at the anniversary date. Remove them from the plan to continue."                                                                   | Remove the products named in the message.                                                                                                |
| "The renewal plan has no changes to submit."                                                                                                                                             | Change at least one subscription or add a product before you place the renewal.                                                          |
| "The code you have entered, \<code>, is not known. …"                                                                                                                                    | Check the code. You can still place the order, but an invalid code makes the order fail.                                                 |
| "Reusable discounts you already hold no longer qualify for this renewal and were not applied: \<codes>."                                                                                 | No action is needed. The renewal is priced without those codes.                                                                          |
| "Adobe rejected the following discount codes: …"                                                                                                                                         | Remove the codes listed, or choose another code for those items.                                                                         |

### Upgrade wizard messages

The following table describes the messages you might see in the upgrade wizard:

| Message                                                                                                                                                                             | What to do                                                                        |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| "A renewal has been set up for this agreement's anniversary date, so the subscription cannot be upgraded until it takes effect. To change the renewal, re-open the renewal wizard." | Upgrade after your anniversary date, or change the renewal in the renewal wizard. |
| "An early renewal has already been placed for this agreement, so the subscription cannot be upgraded until it takes effect at the anniversary date. …"                              | Upgrades are possible again 30 days after the early renewal.                      |
| "No upgrades available"                                                                                                                                                             | Adobe does not offer an upgrade for this product.                                 |
| "The mid-term upgrade is available to client accounts only."                                                                                                                        | Sign in with your client account.                                                 |

### Government products

<details>

<summary>"This Adobe account is for a Large Government Agency. Please use the Adobe VIP Marketplace for Large Government Agencies product." (VIPM0038)</summary>

**Cause** – You ordered a Large Government Agency account with the wrong product.

**Resolution** – Place the order with the **Adobe VIP Marketplace for Large Government Agencies** product.

</details>

<details>

<summary>"This Adobe account is a Government account. Please use the Adobe VIP Marketplace for Government product." (VIPM0039)</summary>

**Cause** – You ordered a Government account with the wrong product.

**Resolution** – Place the order with the **Adobe VIP Marketplace for Government** product.

</details>

<details>

<summary>"The quantity selected must be greater than 100 licenses for Large Government Agency." (VIPM0040)</summary>

**Cause** – Large Government Agency orders need at least 100 licenses.

**Resolution** – Order 100 or more licenses.

</details>

<details>

<summary>"The Agency type is not valid: This parameter is mandatory and must be: FEDERAL, STATE." (VIPM0005)</summary>

**Cause** – The agency type is missing.

**Resolution** – Select **Federal** or **State**, then select **Process** on the order.

</details>

### Migrating from VIP and transferring your reseller

<details>

<summary>"The &#x3C;field> is not valid: &#x3C;details>." (VIPM0005)</summary>

**Cause** – Adobe could not find the VIP membership number, or could not use it. If the details say "Migration in progress, retry later", Adobe is still migrating the account.

**Resolution** – Check the membership number and correct it. If a migration is in progress, wait and try again later.

</details>

<details>

<summary>"No active items have been found for this membership." (VIPM0018)</summary>

**Cause** – The VIP membership has no active subscriptions to migrate.

**Resolution** – Check the membership number. Contact SoftwareOne if you need help.

</details>

<details>

<summary>"The items owned by the given membership don't match the order (sku or quantity): &#x3C;lines>." (VIPM0029)</summary>

**Cause** – The items or quantities in the order don't match the subscriptions in the VIP membership.

**Resolution** – Contact SoftwareOne.

</details>

<details>

<summary>"Membership has already been migrated." (VIPM0030)</summary>

**Cause** – This VIP membership has already moved to VIP Marketplace.

**Resolution** – No migration is needed. Contact SoftwareOne if you cannot see the agreement.

</details>

<details>

<summary>"Do not add or remove items, and do not modify the quantities of any items. You may make these changes using a Change order once this order completes." (VIPM0021)</summary>

**Cause** – You changed the items or quantities in a migration or activation order.

**Resolution** – Keep the order as it is. After it completes, make your changes with a change order.

</details>

<details>

<summary>"Customer account is inactive or blocked. Adobe status code is &#x3C;status>." (VIPM0007)</summary>

**Cause** – Adobe has marked the account as inactive or blocked.

**Resolution** – Contact SoftwareOne.

</details>

<details>

<summary>"Error processing the reseller change code &#x3C;code>: &#x3C;details>" (VIPM0036)</summary>

**Cause** – Adobe did not accept the reseller change code, for example, because it has expired.

**Resolution** – Generate a new code in the Adobe Admin Console, then place the order again. For more details, see [Transfer your Adobe account to SoftwareOne](set-up-your-account/transfer-your-adobe-account-to-softwareone.md).

</details>

<details>

<summary>"Due to reseller change requirements, it is not possible to add additional items to this order. Only the automatically included item can be processed" (VIPM0036)</summary>

**Cause** – You added items to a reseller transfer order.

**Resolution** – Remove the extra items. After the transfer completes, add them with a change order.

</details>

<details>

<summary>"The customer admin Email is not valid" (VIPM0037)</summary>

**Cause** – Adobe did not accept the administrator email address for this account.

**Resolution** – Check the email address in the Adobe Admin Console, under **Users** > **Administrators**, then place the order again.

</details>

### End-of-sale products

<details>

<summary>"The following SKUs are expired: &#x3C;SKUs>. Available SKUs: &#x3C;SKUs>." (VIPM0038)</summary>

**Cause** – Adobe no longer sells the item you ordered.

**Resolution** – Choose one of the available items listed in the message.

</details>

### Other errors

If you see an error that isn't listed here, such as "Order can't be processed. Failure reason: …" or a message that includes "Adobe returned an error", contact SoftwareOne. Include the order ID and the full message.

### Related topics

* [Returns and termination](returns-and-termination/)
* [Key dates and deadlines](key-dates-and-deadlines.md)
