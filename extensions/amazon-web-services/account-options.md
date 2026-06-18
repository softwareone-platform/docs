---
description: Learn about the different AWS account options in the Marketplace.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# AWS account setup options

When you are ordering AWS services through the SoftwareOne Marketplace, you can either create a new AWS account or transfer billing of your Management Account to SoftwareOne.&#x20;

This topic describes how these options work and what is required to complete the setup.

{% hint style="info" %}
When you purchase AWS services through the Marketplace, SoftwareOne does not assume administrative access to your AWS accounts.
{% endhint %}

### Create a new AWS account

Creating a new AWS account means [signing up for AWS ](https://signin.aws.amazon.com/signup?request_type=register)through SoftwareOne.&#x20;

To create an account, AWS requires the following details:

* **Root user email address** – A unique email address for the AWS root user. Use a corporate alias instead of your personal email address. This ensures your company retains control of accounts even if an employee leaves.
* **AWS account name** – A descriptive name used to identify the account within AWS and AWS Organizations.
* **A valid credit card** – Required by AWS for identity verification during account creation.

After creating the account, complete the required AWS setup steps and prepare your new account for onboarding before connecting it to SoftwareOne.

#### Prepare your new AWS account for onboarding

After signing in to your new AWS account:

1. **Secure the root user account**
   * Enable multi-factor authentication (MFA) for the root user.
   * Store root credentials securely.
   * Avoid using the root user for daily activities.
2. **Enable AWS Organizations**
   * In the AWS Management Console, open **AWS Organizations**.
   * Enable **All features**.&#x20;
   * This account becomes the AWS Organizations management account.
3.  **Enable required organizational services**

    To support secure onboarding and automated deployment, enable:

    * **Service Control Policies (SCPs)** in AWS Organizations.
    * **AWS CloudTrail** as an organizational service.
    * **AWS CloudFormation StackSets** in both AWS Organizations and the AWS CloudFormation console.
    * **IAM access to Billing and Cost Management** to access billing data.

For detailed instructions, see [AWS Organizations requirements](aws-organizations-requirements.md).

After completing these steps, copy the 12-digit AWS Organizations management account ID and return to the SoftwareOne Marketplace purchase flow to continue onboarding.

For step-by-step instructions on creating and transferring the new AWS account, see [Sign up for a new AWS account](tutorials/sign-up-for-new-aws-account.md).

### Transfer your existing AWS account

Existing AWS customers can transfer the billing for their existing AWS Management Account to SoftwareOne.

To start the transfer, provide the 12-digit AWS Management Account ID in the SoftwareOne Marketplace purchase flow and complete the guided transfer steps.&#x20;

To complete the process successfully:

* An administrator of this management account must approve the billing transfer invitation, sent by AWS to the root account alias.&#x20;
* The [Essentials Bootstrap Role](https://docs.softwareone.cloud/knowledge-base/essentials-bootstrap-role-customer-manual) must be deployed to enable SoftwareOne to deliver our services and support.&#x20;

For more details on the billing transfer process, see this [official AWS announcement](https://aws.amazon.com/about-aws/whats-new/2025/11/billing-transfer-multi-organization-billing-cost-management/). To transfer your account to SoftwareOne, see [Transfer your AWS account](tutorials/transfer-your-aws-account.md).
