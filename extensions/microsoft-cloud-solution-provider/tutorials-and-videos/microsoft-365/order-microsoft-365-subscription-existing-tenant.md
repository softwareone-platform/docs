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

In this step, do the following:

1. Sign in to your account and go to the **Products** page.&#x20;
2. Select the **Microsoft 365 Business, Enterprise & Apps - Commercial** product. The details page of your selected product opens.&#x20;
3. Click **Buy now** in the upper right. The purchase wizard starts.
{% endstep %}

{% step %}
### Create the agreement

The **Select agreement** step is the first step that is displayed when the purchase wizard starts.

In this step, click **Create agreement** to begin creating your new agreement.  You'll then be directed to the **Select licensee** step of the wizard.
{% endstep %}

{% step %}
### Select licensee

In this step, choose the licensee you want to use and click **Next**.&#x20;

In this tutorial, we'll select an existing licensee. However, you can add a new licensee by clicking **Add licensee** and following the instructions in [Create Licensees](../../../../modules-and-features/settings/licensees/create-licensees.md).
{% endstep %}

{% step %}
### Connect your Microsoft tenant

In this step, select the **Connect existing cloud account** option to connect your existing tenant and click **Next**.&#x20;

Note that if you select this option, the global administrator of your Microsoft account will need to accept the relationship request.
{% endstep %}

{% step %}
### Enter your Microsoft account details

In this step, do the following:

1. Enter the name of your existing tenant.
2. Fill out the contact form. You'll need to provide the first and last name, email address and phone number of the person who will manage your account.&#x20;
3. Click **Next**. The platform will validate your Microsoft tenant details. If no tenant is found, a message is displayed. You'll need to fix the error to proceed.
{% endstep %}

{% step %}
### Special qualifications

If your organization is a [state-owned](https://www.microsoft.com/en-us/legal/compliance/anticorruption/criteria) entity, select the **I confirm the Company is a State Owned Entity** checkbox. Otherwise, leave it cleared.&#x20;

A company is classified as state-owned if it is either controlled by the government or performs functions that the government considers its own.
{% endstep %}

{% step %}
### Add support contacts

Enter the contact details of your support administrator and choose your preferred support language. Click **Next** to continue.
{% endstep %}

{% step %}
### Select the required items

In this step, do the following:

1. Choose the items you want to order and then click **Add items**. You can select multiple items. When the items are added, the **Select items** section is displayed.
2. Review and adjust the license quantity as required.
3. If applicable, [read the offer attestation](../../faqs/what-is-offer-attestation.md). The offer attestation is only displayed for Windows 365 Business with the Windows Hybrid Benefit.&#x20;
4. Click **Next** to continue.
{% endstep %}

{% step %}
### Provide reference details

Use this page to enter optional details, like additional IDs or notes related to your purchase, and click **Next**.
{% endstep %}

{% step %}
### Place your order

Review the details of your order. Make sure to read the terms and conditions associated with this purchase, including the privacy statement. By placing the order, you accept all terms.

Click **Place order** to complete your purchase.
{% endstep %}

{% step %}
### View order summary

View your order summary and the latest status message. Click **View Order** to navigate to the order details page. Otherwise, click **Close** to close the **Summary** page.
{% endstep %}
{% endstepper %}

## Next steps

Once you have placed your order, we'll verify the order details, including the Microsoft tenant ID and create your new subscription under your existing tenant. If there are issues with your order, the [order details ](https://docs.platform.softwareone.com/modules-and-features/marketplace/orders#subscription-details)page will provide information about the problem and any actions you may need to take.
