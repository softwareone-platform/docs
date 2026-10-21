# Subscription end date errors

**Error** – "The agreement includes an option to align all subscription end dates. However, the date currently stored in the 'End Date Alignment' parameter is invalid. To provide a valid date, you need to contact support._"_

**Cause** – This error appears when your order is querying for a valid subscription alignment date or when you are creating a new change order. It's related to the date specified in the **End date alignment** parameter of the agreement and could mean any of the following:

* The end date is invalid.
* The parameter information doesn't match an active subscription in that tenant.&#x20;
* The date either refers to a terminated subscription or was entered incorrectly.

**Resolution** – To resolve this issue, [contact support](../../../../../help-and-support/contact-support.md) and provide a valid end date.

To find the cotermination date, in the [Microsoft Admin Portal](https://admin.microsoft.com/), go to **Billing** > **Your products**. Check the renewal or expiration date of an active, license-based subscription to determine the end date and provide it to the Support team.&#x20;

***

**Error** – "The agreement includes an option to align all subscription end dates. However, the date currently stored in the 'End date alignment' parameter is invalid, as yearly subscriptions cannot be aligned with monthly subscriptions. You can either provide a valid date or proceed with the order, in which case the subscription end dates will not be aligned. If you wish to modify the End Date Alignment, please contact our support team."

**Cause** –This error appears when the coterminosity feature is enabled with a monthly term subscription, but a new annual subscription is being ordered as part of a change order.

**Resolution** – To resolve this issue, [contact support](../../../../../help-and-support/contact-support.md) and provide a valid end date so that the cotermination dates can be aligned. If you choose not to align the end dates, you can proceed with the order; however, the subscription will be created without any coterm.

***

**Error** – "Required action: Subscriptions end date alignment is not valid."&#x20;

**Cause** – This error occurs for orders that are querying when the date provided for cotermination is invalid.

**Resolution** - To resolve this issue, [contact support](../../../../../help-and-support/contact-support.md) and provide a valid end date. See the first error message on this page for details on how to determine a valid cotermination date.
