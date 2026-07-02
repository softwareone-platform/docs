# Transfer your AWS account

This tutorial describes how you can transfer the billing and management for your existing AWS Management Account to SoftwareOne by establishing a new agreement.&#x20;

### Prerequisites <a href="#prerequisites" id="prerequisites"></a>

Before starting this tutorial, make sure you have the following:

* The 12-digit Management Account ID of your AWS Organization.
* Contact details for a technical representative within your organization who can act as the deployment point of contact.
* An active licensee in the Marketplace, or permission to [create one](../../../modules-and-features/settings/licensees/create-licensees.md). A licensee is required to create a new agreement.

### Transfer your existing AWS account

{% stepper %}
{% step %}
**Start the guided Purchase workflow for AWS**

To start the purchase wizard:

1. Go to **Catalog** > **Products**.&#x20;
2. Select **Amazon Web Services**.&#x20;
3. Review the information, including product details, features, and more.&#x20;
4. Select **Buy now**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/aws-product-details.png" alt=""><figcaption><p>The Buy now option on the product details page.</p></figcaption></figure></div>
{% endstep %}

{% step %}
**Transfer your existing account**

Complete the following steps to transfer your account:

1. **Select agreement** – Select **Create agreement**.
2. **Select licensee** – Select a licensee. You can also [create a new licensee](https://docs.platform.softwareone.com/~/changes/362/modules-and-features/settings/licensees/create-licensees) and select that licensee when it appears in the list. Select **Next**.
3. **Create agreement** – Select **Transfer an existing AWS account**, then select **Next**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/aws-transfer-account-option.png" alt=""><figcaption><p>Select the option to transfer your account.</p></figcaption></figure></div>

4. **AWS details** – Complete the following steps:
   1. Provide the 12-digit AWS Management Account ID of your AWS organization.
   2. Review and update the contact form as necessary.
   3. Select **Next**.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/aws-transfer-account.png" alt=""><figcaption><p>Provide your Management Account ID and required contact details.</p></figcaption></figure></div>

5. **Support details** – Select **SoftwareOne Enterprise Support** or **AWS Resold Support**, then select **Next**.
6. **Cost management** – Review the available Cost Management tools, including [FinOps for Cloud](../../finops-for-cloud/). Both options are selected by default and cannot be changed. Select **Next**.
7. **Supplementary services** – Choose any additional AWS services you are interested in and select **Next**. Your selection indicates interest only; no services are provisioned at this stage. A SoftwareOne representative will contact you to provide more information.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/aws-supplementary-services.png" alt=""><figcaption><p>Select any additional AWS services you are interested in.</p></figcaption></figure></div>

8. **Items** – Review the AWS Service item in your agreement. Do not remove this item. Select **Next**.
9. **Details** – Provide reference details, such as additional IDs or notes, and select **Next**.
10. **Review order** – Read the terms and conditions and the privacy statement. When done, select **Place order** to submit your order.
{% endstep %}
{% endstepper %}

### Next steps

After placing the order, you will receive a confirmation message. You can check the order details page for information on the next steps, including:

1. **Accepting the AWS billing transfer invitation** – You will receive an invitation email from AWS. You must accept the invitation so we can proceed with your order.
2. **Approving the service terms** – You will receive an email from AWS, requesting you to accept the minimum service term of your agreement.
3. **Deploying the SoftwareOne Bootstrap role** – After accepting the billing transfer invitation and the service terms, you must deploy the Essentials Bootstrap Role. Deploying this role is mandatory for onboarding. For more details, see [Essentials Bootstrap Role](https://docs.softwareone.cloud/knowledge-base/essentials-bootstrap-role-customer-manual) in SoftwareOne Services documentation.

You will also receive email notifications when these actions are due and require your attention.
