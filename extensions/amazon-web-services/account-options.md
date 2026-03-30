---
description: Learn about the different AWS account options in the Marketplace.
---

# AWS account setup options

When you are ordering AWS services through the SoftwareOne Marketplace, you can either create a new AWS account or transfer billing of your Management Account to SoftwareOne. This topic describes how these options work and what's needed to complete the setup.

{% hint style="success" %}
When you buy AWS services from Marketplace, SoftwareOne does not assume administrative access to your AWS accounts, unlike in previous AWS partner models.
{% endhint %}

### New AWS account

Creating a new AWS account means you want to [sign up for AWS ](https://signin.aws.amazon.com/signup?request_type=register)through SoftwareOne.&#x20;

To create an account, AWS requires the following details:

* Your unique root user email address. It's important to use a corporate alias instead of your personal email address. This ensures your company retains control of accounts even if an employee leaves.
* AWS account name.
* A valid credit card.

Once the account is created, you can use it to [create a new AWS Organization](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tutorials_basic.html#tutorial-orgs-step1). You can then use the 12-digit AWS Account ID to connect with SoftwareOne through the Marketplace platform.&#x20;

For details on creating a new account and then transferring this newly created account to SoftwareOne, see [Sign up for new AWS account](tutorials/sign-up-for-new-aws-account.md).

### Transfer your existing AWS account

Existing AWS customers can transfer the billing for their existing AWS Management Account to SoftwareOne.

You can do this by providing the 12-digit AWS Management Account ID in the Purchase Wizard of SoftwareOne Marketplace and completing the guided steps.&#x20;

To complete the transfer process successfully, an administrator of this Management Account must approve the billing transfer invitation, sent by AWS to the root account alias. Additionally, the [Essentials Bootstrap Role](https://docs.softwareone.cloud/knowledge-base/essentials-bootstrap-role-customer-manual) must be deployed, so we can deliver all of our services and support to you.&#x20;

For more information on the billing transfer process, read this [official AWS announcement](https://aws.amazon.com/about-aws/whats-new/2025/11/billing-transfer-multi-organization-billing-cost-management/). For details on transferring your account to SoftwareOne, see [Transfer your AWS account](tutorials/transfer-your-aws-account.md).
