# Order Microsoft 365 Subscription For Existing Tenant

This tutorial guides you through the steps to order a Microsoft 365 subscription by creating a new agreement.

When establishing a new agreement with SoftwareOne, you can either establish a new Microsoft account or use an existing one. In this tutorial, you'll connect your existing cloud account.&#x20;

{% embed url="https://vimeo.com/985744841/f08189d1c0" %}
Video tutorial: How to order Microsoft 365 subscription for an existing tenant
{% endembed %}

## Prerequisites <a href="#howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites" id="howtoorderamicrosoft365subscriptionforanexistingmicrosofttenant-prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* Your Microsoft tenant name.&#x20;
* A Marketplace licensee in the **active** state or permission to [create a new licensee](../../../../modules-and-features/settings/licensees/create-licensees.md) (if you don't want to use an existing licensee). You'll need to select the licensee when you are creating the agreement.&#x20;

## Implementation

{% stepper %}
{% step %}
### Launch the purchase wizard <a href="#launch-the-purchase-wizard" id="launch-the-purchase-wizard"></a>

1. Sign in to your account and go to the **Products** page.&#x20;
2. Select **Microsoft 365 Business, Enterprise & Apps - Commercial**. The details page of your selected product opens.&#x20;
3. On the details page, select **Buy now** to start the purchase wizard.
{% endstep %}

{% step %}
### Create the agreement

The **Select agreement** page is the first page in the purchase wizard.

Select **Create agreement** to start creating your new agreement.
{% endstep %}

{% step %}
### Select licensee

Choose the licensee you want to use and select **Next**.&#x20;

In this tutorial, we'll select an existing licensee. However, you can add a new licensee by selecting **Add licensee** and following the instructions in [Create Licensees](../../../../modules-and-features/settings/licensees/create-licensees.md).
{% endstep %}

{% step %}
### Connect your Microsoft tenant

Select **Connect existing cloud account** to connect your existing tenant. Then, select **Next**.&#x20;

Note that if you select this option, the global administrator of your Microsoft account will need to accept the relationship request.
{% endstep %}

{% step %}
### Enter your Microsoft account details

Complete the following steps:

1. Enter the name of your existing tenant.
2. Fill out the contact form. You'll need to provide the first and last name, email address, and phone number of the person who will manage your account.&#x20;
3. Select **Next**. The platform will validate your Microsoft tenant details. If no tenant is found, a message is displayed. You'll need to fix the error to proceed.
{% endstep %}

{% step %}
### Special qualifications

If your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity, select the **I confirm the Company is a State Owned Entity** checkbox. Otherwise, leave it cleared.&#x20;

A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
{% endstep %}

{% step %}
### Add support contacts

Enter the contact details of your support administrator and choose your preferred support language. Select **Next**.
{% endstep %}

{% step %}
### Select the required items

Complete the following steps:

1. Choose the items you want to order and then select **Add items**. You can select multiple items. When the items are added, the **Select items** section is displayed.
2. Review and adjust the license quantity as required.
3. If applicable, [read the offer attestation](broken-reference). The offer attestation is only displayed for Windows 365 Business with the Windows Hybrid Benefit.&#x20;
4. Select **Next**.
{% endstep %}

{% step %}
### Provide reference details

Enter optional details, like additional IDs or notes related to your purchase, and select **Next**.
{% endstep %}

{% step %}
### Place your order

1. Review the details of your order. Make sure to read the terms and conditions associated with this purchase, including the privacy statement. By placing the order, you accept all terms.
2. Select **Place order**.
{% endstep %}
{% endstepper %}

## Next steps

Once you have placed your order, we'll verify the order details, including the Microsoft tenant ID and create your new subscription under your existing tenant. If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.
