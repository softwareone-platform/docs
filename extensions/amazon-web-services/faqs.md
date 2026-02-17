# FAQs

### Product Overview & Availability

<details>

<summary>What new product for AWS has been launched on the SoftwareOne Marketplace?</summary>

We are launching **Amazon Web Services and SoftwareOne Cloud Managed Services Essentials** through the SoftwareOne Marketplace. This offering combines the newly launched [AWS Billing Transfer](https://aws.amazon.com/about-aws/whats-new/2025/11/billing-transfer-multi-organization-billing-cost-management/) feature with SoftwareOne service offerings related to AWS.

</details>

<details>

<summary>In which regions will the new product be available?</summary>

The new product, **Amazon Web Services and SoftwareOne Cloud Managed Services Essentials**, is available in all AWS regions that support [Billing Transfer](https://aws.amazon.com/about-aws/whats-new/2025/11/billing-transfer-multi-organization-billing-cost-management/). This includes all public AWS regions, except AWS GovCloud (US) and China (Beijing and Ningxia) regions.&#x20;

Additionally, the product is available in countries where SoftwareOne has a presence so that invoices can be issued.

</details>

<details>

<summary>What happens to the former Marketplace product?</summary>

The former product, **Amazon Web Services - Managed Service**, based on the ECAM model, is still available to customers with an active agreement for this product.

However, if you are a new customer, you must sign up for the **Amazon Web Services and SoftwareOne Cloud Managed Services Essentials** agreement, which is based on AWS billing transfer starting February 19, 2026.

</details>

<details>

<summary>Will there be a transition from the former product to the new one?</summary>

Yes, we will transition existing customers to the new offering through the SoftwareOne Marketplace in due course. However, this depends on various legal and commercial factors.

</details>

<details>

<summary>Does the SoftwareOne Marketplace cover all AWS account types?</summary>

The SoftwareOne Marketplace covers all AWS Commercial accounts, except:

* AWS Private Pricing Agreements (PPA) customers
* AWS China (Beijing and Ningxia) region accounts
* AWS GovCloud (US)
* Tier 2 resale model AWS accounts

Government customers are advised to contact their SoftwareOne account manager before purchasing AWS through the SoftwareOne Marketplace.

Due to the [AWS Billing Transfer](https://aws.amazon.com/about-aws/whats-new/2025/11/billing-transfer-multi-organization-billing-cost-management/) feature, other partner model account types, including End-Customer Account Model (ECAM) and Solution Provider Account Model (SPAM), are being phased out by AWS.

Additionally, capabilities to add the AWS reseller model (tier 2) to billing transfer are planned by AWS, but are not yet available.

{% hint style="info" %}
To make use of billing transfer, an AWS account must be a management account.
{% endhint %}

</details>

<details>

<summary>Can Private Pricing Agreement (PPA), formerly Enterprise Discount Program (EDP), customers buy this product in the SoftwareOne Marketplace?</summary>

Not yet.&#x20;

Currently, AWS PPA customers, who were previously part of EDP, are expected to have the billing transfer capability by AWS in 2026. However, at this time, PPA customers are not supported by the SoftwareOne marketplace.&#x20;

We aim to be ready when PPA is added to the billing transfer by AWS or shortly after.

</details>

### Purchasing, Setup, & Billing Transfer

<details>

<summary>How do I buy Amazon Web Services and SoftwareOne Cloud Managed Services Essentials?</summary>

You can purchase **Amazon Web Services and SoftwareOne Cloud Managed Services Essentials** by searching for the product in our catalog and going through the Purchase Wizard.&#x20;

Alternatively, SoftwareOne Operations can prepare a draft order on your behalf and send it to you for acceptance via a link. You must complete and submit the draft order yourself, as it requires accepting the terms and conditions for both the SoftwareOne Marketplace and Services.&#x20;

To learn more, see [Sign Up for New AWS Account](tutorials/sign-up-for-new-aws-account.md) and [Transfer Your AWS Accoun](tutorials/transfer-your-aws-account.md)t.

</details>

<details>

<summary>I already have an AWS organization. How do I buy Amazon Web Services and SoftwareOne Cloud Managed Services Essentials?</summary>

If you already have an AWS organization, you can choose the **Transfer an existing AWS account** option in the Purchase Wizard. This allows you to connect your AWS organization to SoftwareOne via billing transfer.

For more information, see [Transfer Your AWS Account](tutorials/transfer-your-aws-account.md).

</details>

<details>

<summary>I don't have an AWS account. How do I buy Amazon Web Services and SoftwareOne Cloud Managed Services Essentials, and how do I connect to SoftwareOne?</summary>

If you don't have an account with AWS, or you prefer to connect a whole new AWS organization to SoftwareOne, you can choose the **Create a new AWS account** option in the Purchase Wizard.

You will then see a message with instructions on how to create a new AWS account and convert it to a management account.

For details, see [Sign Up for New AWS Account](tutorials/sign-up-for-new-aws-account.md).

</details>

<details>

<summary>What actions do I need to take to order Amazon Web Services and SoftwareOne Cloud Managed Services Essentials?</summary>

While we aim to automate as many steps as possible and make the process easy, certain actions are still required depending on your specific scenario.&#x20;

You are required to:

* Start the Purchase Wizard in the SoftwareOne Marketplace.
* Have an existing AWS account or create a new one.
* Accept the SoftwareOne Terms and Conditions when submitting your order.
* Accept the billing transfer request to connect your AWS account to SoftwareOne.
* Accept the service term (12 months by default).
* Deploy the required SoftwareOne roles for service delivery (AWS Essentials).

You must also have the correct permissions on your AWS account to complete all steps.&#x20;

Once these steps are completed, your order is finalized, and the agreement becomes active in the SoftwareOne Marketplace.

Billing begins at the start of the next billing cycle and includes a minimum commitment of 12 AWS billing cycles (calendar months).

</details>

<details>

<summary>What happens if I don't complete all the steps required to place an order?</summary>

We send timely reminders to help you finalize and submit your order.&#x20;

If certain steps remain incomplete, your order for **Amazon Web Services and SoftwareOne Cloud Managed Services Essentials** might be rejected.&#x20;

For example, if the billing transfer request is not accepted, the order fails. The order also fails if you don't deploy the [Bootstrap Role](https://docs.softwareone.cloud/knowledge-base/essentials-bootstrap-role-customer-manual) in your environment and have opted for SoftwareOne Enterprise Support for AWS.

</details>

<details>

<summary>I didn’t receive any service term (handshake) email? How long should I wait for the email to arrive?</summary>

After you accept the billing transfer invitation from AWS, it can take some time to receive the service term (handshake) email. This is expected and typically takes around 15 minutes. The handshake invitation is sent by AWS to the same email address that received the billing transfer request.

If you prefer not to wait, you can select **Process** in the upper-right corner of your AWS Marketplace order. This will prompt the platform to validate the billing acceptance and proceed to the next step.

</details>

<details>

<summary>I didn't receive the billing transfer email.</summary>

Ensure you have access to the email address registered as the root for the AWS organizational account you are trying to connect with SoftwareOne.

If you have access but are not receiving emails, including in your spam or junk folder, contact [SoftwareOne Marketplace Platform Support](../../help-and-support/contact-support.md) or your account manager. It could be possible that the account ID you are trying to connect is not eligible for billing transfer.

</details>

<details>

<summary>I receive an error when accepting the billing transfer email.</summary>

If you receive an error, check that you have the rights to accept the AWS invite for the AWS account you are trying to connect with SoftwareOne.&#x20;

Additionally, check that you are not restricted by another AWS provider from switching partners. Sometimes, when an AWS account tries to connect multiple times to the same partner management account of SoftwareOne, an existing billing transfer invite (even expired) can cause new invitations to fail.&#x20;

In such cases, contact [SoftwareOne Marketplace Platform Support](../../help-and-support/contact-support.md).

</details>

<details>

<summary>I receive an error when accepting the handshake or invitation e-mail.</summary>

To avoid common errors with the AWS billing transfer invitation, ensure you are using the correct AWS account and credentials when accepting the handshake.&#x20;

If you have any questions or encounter issues, contact [SoftwareOne Marketplace Platform Support](../../help-and-support/contact-support.md).

</details>

### Billing & Invoicing

<details>

<summary>How does billing work?</summary>

You receive a monthly invoice that includes your charges for standard resource usage, Reserved Instances, AWS Marketplace purchases, and any other applicable charges, as well as any discounts provided by SoftwareOne.

Your first SoftwareOne invoice could be issued up to two months after you accept the billing transfer request, due to AWS billing processes operating in the background.

</details>

<details>

<summary>When will I receive my first invoice from SoftwareOne?</summary>

This is determined by the month in which you receive and accept the AWS billing transfer request.&#x20;

The billing transfer starts on the 1st of the calendar month following acceptance. Then, SoftwareOne must wait for a full calendar month to receive the charges for that first full monthly period from AWS. Once we receive these charges, you will be invoiced. All subsequent invoices are issued monthly.

For example, if the billing transfer request is accepted on February 19, 2026, the billing transfer starts on March 1, 2026. SoftwareOne receives the AWS invoice for the March charges on April 1, 2026, and invoices you shortly after.

</details>

<details>

<summary>Where can I see my invoices?</summary>

You can access your invoices on the [Invoices page](../../modules-and-features/marketplace/billing/invoices/) in the SoftwareOne Marketplace.&#x20;

</details>

<details>

<summary>When will the billing by SoftwareOne stop?</summary>

Your billing relationship with SoftwareOne ends when the billing transfer term expires. This is at the end of the calendar month in which either SoftwareOne or you remove the billing transfer relationship.

A final invoice covering charges for that last month is issued during the following calendar month’s billing cycle (in arrears).

</details>

<details>

<summary>Where can I see my cloud spending?</summary>

You can view your cloud spend analysis in [SoftwareOne's FinOps for Cloud](https://docs.finops.softwareone.com/) platform.

</details>

<details>

<summary>I want another billing currency for my AWS invoices from SoftwareOne than the one displayed in the Marketplace during purchase.</summary>

In such cases, you can contact your SoftwareOne account manager.&#x20;

They will check whether the desired currency option is available through SoftwareOne and guide you through the rest of the process.&#x20;

If the currency is supported, you will see your agreement in that currency in your Marketplace account once the process is complete.

</details>

### Support Options

<details>

<summary>What support options are available when purchasing AWS through SoftwareOne?</summary>

During the purchase process, you can choose between two support options:

* **SoftwareOne Enterprise Support for AWS (Partner-Led Support or PLS)** - Support is delivered directly by SoftwareOne, providing a partner-led experience.
* **AWS Resold Support** - Standard AWS support services delivered directly by AWS.

To learn more, see [AWS support levels](aws-concepts.md#resold-vs-partner-led-aws-support).

</details>

<details>

<summary>How do I get technical support?</summary>

You can get support by contacting [SoftwareOne Marketplace Platform Support](../../help-and-support/contact-support.md), as well as [SoftwareOne Services Technical Support](https://docs.softwareone.cloud/knowledge-base/contacting-softwareone-support).&#x20;

SoftwareOne Enterprise Support for AWS customers also get access to a dedicated services portal to submit tickets.

</details>

### Agreement & Service Terms

<details>

<summary>When does the SoftwareOne agreement stop?</summary>

The agreement remains active indefinitely and only expires when either party terminates the relationship and order.&#x20;

A default minimum period of 12 months is added after a successful purchase.

</details>

<details>

<summary>Is there a minimum service period?</summary>

Yes, the standard 12-month minimum service period for essentials applies.&#x20;

This period is enforced through a handshake invitation immediately after acceptance of the billing transfer.

</details>

<details>

<summary>How to offboard AWS (legacy and new purchases)?</summary>

To offboard, you must place a termination order through the SoftwareOne Marketplace. Once you place the order, we will review it in line with your active service term.

</details>

### Security, Access, & Roles

<details>

<summary>Which roles get deployed within our environment?</summary>

See the [Essentials Bootstrap Role](https://docs.softwareone.cloud/knowledge-base/essentials-bootstrap-role-customer-manual) page in the SoftwareOne Services documentation.

</details>

<details>

<summary>Does SoftwareOne have access to my environment?</summary>

SoftwareOne has access only through the deployment of the SoftwareOne Bootstrap Role.&#x20;

For details, see the [Essentials Bootstrap Role](https://docs.softwareone.cloud/knowledge-base/essentials-bootstrap-role-customer-manual) page in the SoftwareOne Services documentation.

</details>

<details>

<summary>Does SoftwareOne have access to my AWS root account?</summary>

No, SoftwareOne doesn't own the root credentials of customer accounts. You don't need to share these credentials with us.

This is a fundamental difference with the legacy AWS Solution Provider Program (SPP) offering ECAM (End-Customer Account Model) and SPAM (Solution Provider Account Model).

</details>
