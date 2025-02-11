# Release Notes

## Release Date: 12 February 2025 <a href="#release-date-12-february-2025" id="release-date-12-february-2025"></a>

### Software Subscriptions

We are excited to announce the upcoming launch of Microsoft Software Subscriptions in the Marketplace Platform.

With this update, you can create agreements and purchase nearly the entire suite of Microsoft Server Subscriptions directly through the Microsoft CSP program using our platform. You can also place change orders to add more software subscriptions to your existing agreements. For details, see [Manage Software Subscriptions](software-subscriptions/manage-software-subscriptions.md).

{% hint style="info" %}
Software products with one-time payments are not yet supported.
{% endhint %}

***

## Release Date: 3 February 2025 <a href="#release-date-3-february-2025" id="release-date-3-february-2025"></a>

### New Agreement Restrictions for CSP Products

The creation of new agreements for CSP products using the same CSP domain across multiple clients is now restricted.

Additionally, creating additional agreements using the same CSP tenant, product, and licensee is also prohibited. If an agreement already exists, you must update the existing agreement to request new subscriptions, instead of creating a new one.

***

## Release Date: 28 January 2025 <a href="#release-date-28-january-2025" id="release-date-28-january-2025"></a>

### NCE Auto-applicable Promotions

Marketplace clients who have an existing CSP tenant can check their eligibility for an automatically applicable NCE promotion.&#x20;

If eligible, the updated price is shown in the order. However, if you qualify but don't meet the minimum or maximum license requirements, a message will inform you of the necessary criteria.

### CSP Relationship Request

If an order remains pending for more than 15 days due to an unresolved CSP reselling relationship, it will now be marked as **Failed**.

***

## Release Date: 23 January 2025

### Microsoft Perpetual Software

We are pleased to announce the release of three new products in the Marketplace Platform: Microsoft Perpetual Software for Commercial, Microsoft Perpetual Software for Education, and Microsoft Perpetual Software for Education for Charity.&#x20;

With this release, you can effortlessly create agreements and purchase the full suite of Microsoft Perpetual Software directly through the CSP program in the Marketplace Platform. You can also place change orders to add more perpetual software products to your existing agreements.

This release further expands our product offerings, reinforcing our commitment to delivering comprehensive software solutions through the Marketplace. To learn more, see [Perpetual Software](perpetual-software/) and [Buy Perpetual Software Licenses](tutorials-and-videos/perpetual-software/buy-perpetual-software-licenses.md).

***

## Release Date: 9 December 2024

### Azure Lighthouse Onboarding Automation

[Microsoft Azure Lighthouse](azure-lighthouse/) allows authorized SoftwareOne associates to access your Azure resources seamlessly and securely.&#x20;

As a client, you can authorize SoftwareOne to manage your Azure environment by accepting our Lighthouse access request and completing the necessary onboarding steps. Requests can be accepted by navigating to the **General** tab of a purchase order and following the onboarding instructions. For details, see [Complete the Azure Lighthouse Activation](azure-lighthouse/complete-the-azure-lighthouse-onboarding.md).

Note that until the onboarding process is complete, any purchase orders for newly provisioned Azure subscriptions will display a **Querying** status on the platform. After completing the Lighthouse access request, be sure to update your order's status to **Processing**. For instructions, see [Change Your Order's Status to Processing](../../modules-and-features/marketplace/orders/set-an-order-to-processing.md).

***

## Release Date: 26 November 2024

### State Owned Entity (SOE) Qualification

Global regulatory oversight is increasing, and companies may be required to demonstrate that they have robust policies and processes in place to mitigate the risks of corruption and bribery. A critical first step in this process is the accurate identification of government entities, government-affiliated organizations, and their employees.

To streamline this, Marketplace clients will now have the option to specify whether a company is state-owned in new agreements. A company qualifies as state-owned if it's either directly controlled by the government or performs functions that are considered to be inherently governmental.

To learn about the eligibility criteria for state-owned entities, see[ Microsoft's State Owned Entity Criteria](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria?oneroute=true).

***

## Release Date: 15 October 2024

### New Process Flow

We've updated the provisioning flow for Microsoft product purchase orders. Previously, the process was delayed by Granular Delegated Admin Privileges (GDAP) management, which could take up to 21 days. Now, the provisioning process will no longer wait for GDAP approval to complete the order. A time limit has been set, counting from the order creation in the Microsoft Partner Center, after which the order will be completed regardless of GDAP status.

Note that this does not remove the need for GDAP approval. For cases where approval is delayed or pending, services dependent on GDAP will remain inactive until approval is obtained. The sync process will be updated to handle such cases accordingly.

### Validations and Constraints

To enhance the efficiency and accuracy of purchase and change order fulfillment, updates have been made to the key validation processes. These improvements are designed to streamline the purchasing experience by reducing unnecessary delays and simplifying the workflow for existing users and accounts. The updates include:

* **Cart validation for existing users** - Ensuring that the items in the cart meet the requirements for processing, providing a smoother purchasing and fulfillment experience.
* **Billing profile validation for existing accounts** - Verifying that the Microsoft account billing profile is complete, reducing the risk of fulfillment delays.
* **Microsoft client agreement (MCA) validation** - Ensuring compliance with the Microsoft client Agreement, allowing for a more efficient order-handling process.
* **Removal of validation on ordering parameters for existing agreements** - This change eliminates redundant checks on established agreements, speeding up order processing for returning clients.

These updates aim to improve the fulfillment process by minimizing manual interventions and enhancing the overall client journey for CSP orders in the Marketplace.

### Support for Vanity (non .onmicrosoft.com) Domains

We have introduced an enhancement for existing CSP clients creating new agreements. Clients can now use their **vanity domain** (like, `<http://mybusiness.com>`) as the principal domain, instead of the default `mybusiness.onmicrosoft.com`.

This enhancement allows the SoftwareOne Marketplace to support Microsoft’s effort to create a more customized and professional experience by enabling businesses to represent themselves using their branded domain throughout the agreement creation process. This enhances brand consistency but also simplifies domain management for clients with established vanity domains.

### Subscription Fulfillment Parameters

We are introducing new parameters to enhance the subscription fulfillment process, improving tracking, accuracy, and transparency in subscription management. The new parameters are as follows:

* **Last successful sync** - This parameter stores the timestamp of the most recent successful synchronization, making it easier to monitor and resolve any sync-related issues.
* **Current seat quantities** - This parameter tracks the current number of active seats in a subscription, providing real-time visibility into the active usage.
* **Scheduled seat quantities** - This parameter stores the number of seats scheduled for future changes, ensuring that planned adjustments are properly documented and aligned with client expectations.

These updates will streamline subscription management, offering better control and oversight of active and scheduled seat quantities during the fulfillment process.

***

## Release Date: 22 May 2024

### Microsoft Cloud Solution Provider (CSP) Program

The CSP program allows you to purchase Microsoft subscriptions through the Marketplace Platform and self-manage those subscriptions. &#x20;

To learn about the CSP program, see [Microsoft Cloud Solution Provider](./).&#x20;
