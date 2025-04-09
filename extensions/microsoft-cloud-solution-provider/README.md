# Microsoft CSP

The Microsoft CSP program is designed to provide businesses with easy access to Microsoft's cloud services, such as Microsoft 365, Dynamics 365, and Azure, through certified partners.

Working with a CSP provider like SoftwareOne offers numerous benefits and ensures a smooth onboarding process. These include:

* **Tailored solutions** - SoftwareOne can bundle Microsoft cloud services with additional offerings and services, creating customized solutions that meet specific business needs.
* **Expert support** - Gain access to dedicated support from SoftwareOne's experts, who can help with everything from initial setup to ongoing management and technical issues.
* **Simplified billing** - Enjoy the convenience of monthly billing and invoicing, making it easier to manage budgets and expenses.
* **Strategic guidance** - SoftwareOne provides strategic guidance to help businesses optimize their use of Microsoft cloud services, ensuring they get the most value from their investment.
* **Scalability and flexibility** - Easily scale services up or down based on business needs, with the flexibility to adapt to changing requirements.

The Marketplace Platform lets you manage your onboarding process for Microsoft cloud services, from creating a Microsoft organization tenant to accepting the Microsoft Customer Agreement, and more.

You can track your Microsoft subscription purchases and manage the entire subscription lifecycle through the Marketplace Platform.

## CSP product types <a href="#csp-products" id="csp-products"></a>

In the CSP program, various product types (or service types) are available, each with unique benefits and constraints:

* **License-based products (online services)** - Licenses for products such as Office 365 E3 are User Subscription Licenses; you need one license for each user. These products are also known as seat-based offers or license-based services and include all the Office 365, Microsoft 365, Dynamics 365, and Windows 365 products. When an order for a seat/license-based service is placed, a subscription is created. This is essentially a container that holds the licenses that have been ordered. A subscription may only contain a single license type (for example, Office 365 E3) associated with a single commitment term (for example, 1 year) and a single billing frequency (for example, annual).
* **Software subscriptions** - Software Subscriptions are available for Windows Server and SQL Server and for a fixed subscription term of either 1 or 3 years. They give access to the Azure Hybrid Benefit, which means that you may install the products on-premises or use them to license the products within an Azure virtual machine. See [Software Subscriptions](https://docs.platform.softwareone.com/extensions/microsoft-cloud-solution-provider/software-subscriptions) to learn more.
* **Perpetual software** - Perpetual software licenses are licenses for on-premises Microsoft products that you acquire in perpetuity. In the CSP program, the software is license-only (L-only) and does not include the option to add Software Assurance (SA). See [Perpetual software ](https://docs.platform.softwareone.com/extensions/microsoft-cloud-solution-provider/perpetual-software)to learn more.
* **Usage-based (Azure Plan and Entitlements)** - The Azure Plan new commerce experience gives CSP providers access to Azure services at pay-as-you-go (PAYG) rates for CSP clients under the Microsoft Customer Agreement. This plan simplifies the purchase experience. You can have multiple Azure subscriptions in an Azure plan. In this new commerce experience for Azure, Microsoft has aligned to a single global pricing principle, enabling CSP providers to offer Azure at the published prices.

## CSP onboarding with SoftwareOne <a href="#csp-onboarding-with-softwareone" id="csp-onboarding-with-softwareone"></a>

You can execute each step of the onboarding process through the Marketplace Platform.

{% stepper %}
{% step %}
**Creating a Microsoft organization tenant**

1. **Consultation** - SoftwareOne begins with a consultation to understand your business needs and goals.
2. **Setup** - SoftwareOne creates a Microsoft organization tenant for your business. This tenant acts as a dedicated instance within Microsoft's cloud, housing all users, resources, and data.
3. **Configuration** - SoftwareOne configures the tenant to align with your business requirements, ensuring optimal setup for security, compliance, and performance.
{% endstep %}

{% step %}
**Accepting the Microsoft Customer Agreement**

1. **Understanding Terms** - SoftwareOne guides you through the Microsoft Customer Agreement, explaining the terms and conditions for using Microsoft’s cloud services.
2. **Agreement Acceptance** - SoftwareOne assists you in accepting the agreement, which simplifies the purchasing process and provides clear terms regarding service usage, data privacy, and compliance.
{% endstep %}

{% step %}
**Service provisioning and integration**

1. **Service Activation** - Once the tenant is set up and the agreement is accepted, SoftwareOne provisions the required Microsoft cloud services for your business.
2. **Integration** - SoftwareOne integrates these services with your existing systems, ensuring seamless operation and minimal disruption to your business activities.
3. **Customization** - SoftwareOne can further customize the services to meet specific needs, such as setting up user roles, permissions, and additional configurations.
{% endstep %}

{% step %}
**Ongoing support and management**

1. **Training** - SoftwareOne provides training to ensure your team can effectively use the new services.
2. **Continuous Support** - SoftwareOne offers ongoing support to address any issues and provide updates, helping your business adapt and grow with the evolving cloud landscape.
3. **Optimization** - Regular reviews and optimization services are provided to ensure you continue to get the most out of your Microsoft cloud investment.
{% endstep %}
{% endstepper %}

## CSP and Granular Delegated Admin Privileges (GDAP) <a href="#csp-and-granular-delegated-admin-privileges" id="csp-and-granular-delegated-admin-privileges"></a>

GDAP is a security feature that provides CSP providers with the least-privileged access following the Zero Trust cybersecurity protocol. It lets SoftwareOne configure granular and time-bound access to your workloads in production and sandbox environments. See [Granular Delegated Admin Privileges (GDAP)](granular-delegated-admin-privileges-gdap/) to learn more.

## New Commerce Experience (NCE) <a href="#new-commerce-experience" id="new-commerce-experience"></a>

New Commerce Experience (NCE) is a specific update within the CSP program that introduces changes to the pricing, licensing, and billing of Microsoft’s cloud services. See [Microsoft NCE](microsoft-nce/) to learn more.

## Subscription lifecycle states <a href="#subscription-lifecycle-states" id="subscription-lifecycle-states"></a>

When a subscription is created, it can have several states throughout its lifecycle.

### License-based NCE subscriptions states <a href="#license-based-new-commerce-subscription-states" id="license-based-new-commerce-subscription-states"></a>

NCE subscriptions can be in one of these states: **Active**, **Cancelled**, **Suspended**, **Expired**, **Disabled**, or **Deleted**.

<details>

<summary>Active</summary>

Active is the default state for an NCE subscription. Whilst the subscription is in this state:

* Customers can access and use services.
* Admins can access service data and properties.
* Partners can access and make changes to the subscription properties.
* The transacting partner continues to be billed.

</details>

<details>

<summary>Cancelled</summary>

NCE subscriptions can be canceled within the first 7 days following subscription creation or renewal of the subscription.&#x20;

After the 7-day window passes, the subscription can no longer be canceled.&#x20;

* After a subscription is canceled, there is a 7-day grace period in a **Suspended** state where:
  * Customers can continue to access their data.
  * Partner administrators can back up data before it's removed.
  * If the partner purchases the same product/SKU equivalent to the one canceled, customer data and user license assignment settings are automatically restored.
  * If a new purchase is made with a lower number of licenses, customer data, and user license assignment settings will still be retained, and the partner should manage these appropriately.
  * After the 7-day period, these actions are no longer allowed, and data will be removed.

- Transacting partner will no longer be billed (pro-rata charges may apply)

</details>

<details>

<summary>Suspended</summary>

Partners can suspend (previously known as ‘Pause’) a subscription to temporarily make the services unavailable to customers. Whilst the subscription is suspended:

* Customers can no longer access and use services.
* Admins can access service data and properties.
* The transacting partner continues to be billed.
* Partners can reactivate the subscription before the end of its commitment term.
* Partners can cancel the subscription if it is still within the 7-day transaction window.

If the **Suspended** subscription reaches its end date still in the suspended state, it will now move to a 30-day disabled state.

</details>

<details>

<summary>Expired</summary>

Following the end of an **active** subscription term, a 30-day expired state follows. A previously active subscription will enter this state if auto-renew is turned off and the terms end. In these 30 days:

* Users can access files and services.
* Admins can access data.
* Transacting partner won’t be billed.
* Subscription can’t be reactivated.

After 30 days in the expired state, the subscription moves to a 90-day disabled state.

</details>

<details>

<summary>Disabled</summary>

A 30-day disabled state follows the end of a **suspended** subscription term:

* Partners that suspend their subscription leading to the term end will find their suspended subscription moved to this 30-day disabled state.
* After 30 days in the disabled state, the subscription moves to a 90-day disabled state (120 days disabled in total).
* Users can't access files and services, and only admins can access the data.
* Transacting partner won't be billed.
* Subscription cannot be reactivated.

**The 90-day disabled state** follows the 30-day **Expired** or a 30-day **Disabled** state:

* Data is retained for 90 days after the end of the previous state.
* Users can't access files and services, and only admins can access the data.
* Transacting partner won't be billed.
* Subscription can't be reactivated.

</details>

<details>

<summary>Deleted</summary>

After the subscription passes the 90-day disabled state, it stays deleted, which means:

* The subscription is nonrecoverable.
* If the partner cancels their subscription, the subscription will first go into the **Suspended** state for 7 days, and then to **Deleted** where data will be removed.
* Transacting partner won't be billed.
* The subscription cannot be reactivated.

</details>

### License-based legacy subscription states <a href="#license-based-legacy-subscription-states" id="license-based-legacy-subscription-states"></a>

Legacy subscriptions can be in one of these states: **Active**, **Suspended**, or **Deleted**.

<details>

<summary>Active</summary>

In the **Active** state:

* The default (normal) state of a subscription.
* Partners can access and make changes to subscription properties.
* Customers can access and use services.
* Admins can also access service data and properties.
* The transacting partner continues to be billed.

</details>

<details>

<summary>Suspended</summary>

In the **Suspended** state:

* Partners suspend a subscription to temporarily make the services not usable to customers.
* Partners can reactivate the subscription before the end of the term.
* If the subscription is still suspended by the term's end, the subscription is deleted.
* Partners can only reactivate the subscription.
* Customers can no longer access and use services.
* Admins can access service data and properties.
* Transacting partner won't be billed.

</details>

<details>

<summary>Deleted</summary>

After 90 days in the suspended state, the subscription will be deleted and is nonrecoverable.

</details>

## Subscription states in Marketplace <a href="#subscription-states-withing-the-softwareone-marketplace" id="subscription-states-withing-the-softwareone-marketplace"></a>

The following table shows how the Microsoft subscription states are represented in the Marketplace Platform:

| Product type                                                                    | Microsoft states                                                                                              | Marketplace States                                                                                                  |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| <p>License-based New Commerce</p><p>(example: Microsoft 365 / Dynamics 365)</p> | <ul><li>Active</li><li>Cancelled</li><li>Suspended</li><li>Expired</li><li>Disabled</li><li>Deleted</li></ul> | <ul><li>Active</li><li>Active</li><li>Terminated</li><li>Terminated</li><li>Terminated</li><li>Terminated</li></ul> |
| <p>License-based Legacy</p><p>(example: Microsoft 365 / Dynamics 365)</p>       | <ul><li>Active</li><li>Suspended</li><li>Deleted</li></ul>                                                    | <ul><li>Active</li><li>Terminated</li><li>Terminated</li></ul>                                                      |
| <p>Usage-based</p><p>(example: Microsoft Azure)</p>                             | <ul><li>Active/Enabled</li><li>Deleted</li><li>Disabled</li><li>Expired</li></ul>                             | <ul><li>Active</li><li>Terminated</li><li>Terminated</li><li>Terminated</li></ul>                                   |
| <p>Perpetual</p><p>(example: Perpetual Excel license)</p>                       | <ul><li>Active</li><li>Cancelled</li></ul>                                                                    | <ul><li>Active</li><li>Terminated</li></ul>                                                                         |
| <p>Software subscription</p><p>(example: Windows Server CAL 1yr)</p>            | <ul><li>Active</li><li>Cancelled</li></ul>                                                                    | <ul><li>Active</li><li>Terminated</li></ul>                                                                         |

