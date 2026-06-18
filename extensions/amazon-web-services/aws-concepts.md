---
description: Understand key AWS terminology and concepts.
---

# AWS terminology and concepts

This topic covers key concepts and terminology to help you get started with AWS in the SoftwareOne Marketplace.&#x20;

A clear understanding of AWS organizations, account types, billing transfer process, and support models is required to successfully order AWS services from the Marketplace Platform.

### AWS organization

An organization is a collection of AWS accounts that you can manage centrally and organize into a hierarchical, tree-like structure with a main root at the top and organizational units nested under the root.&#x20;

Each account can be placed directly in the root or within one of the organizational units in the hierarchy.

### AWS organizational units

An organizational unit (OU) is a group of AWS accounts within an organization. An OU can also contain other OUs, enabling you to create a hierarchy.

### Account types

When you sign up for Cloud Managed Services for AWS using the Marketplace Platform, you establish a connection between your AWS Organization and a dedicated payer account owned by SoftwareOne.

* **Payer or Management account** – A master payer account plays a crucial role in the AWS organizational structure. It's responsible for consolidating all charges incurred by the linked AWS accounts. This account acts as the central hub to which various linked accounts connect, forming a cohesive AWS organization.
* **Linked account** – These accounts are actively connected to a master payer account. They are responsible for managing specific workloads and utilizing various AWS resources.
* **Standalone account** – A standalone account operates independently of any linked accounts. This type of account is essentially a payer account on its own, provided it has a valid payment method associated with it. AWS requires this to ensure payment processing, so that the account can be billed for the services used. If you are setting up a new AWS account, ensure you have a credit card ready unless you plan to immediately connect it to a master payer account through the **My Organizations** page in the AWS console.

For more information about AWS Organizations concepts and account types, see [Terminology and concepts for AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html).

### AWS billing transfer <a href="#aws-billing-transfer" id="aws-billing-transfer"></a>

When you purchase Cloud Managed Services for AWS from SoftwareOne, you connect the management or payer account from your own AWS organization with a management account from SoftwareOne. This process is called AWS Billing Transfer.&#x20;

This established connection moves the billing from your AWS account to the SoftwareOne account.&#x20;

While you maintain full access to your own AWS Organization, the billing section for all charges billed by AWS to SoftwareOne is no longer visible.&#x20;

Additionally, any cost and usage report you previously configured is removed and must be reconfigured. For more information, see [AWS Billing Transfer](https://aws.amazon.com/aws-cost-management/aws-billing-transfer/).&#x20;

### AWS support levels <a href="#resold-vs-partner-led-aws-support" id="resold-vs-partner-led-aws-support"></a>

When you order AWS services through SoftwareOne, you can choose between two support options:&#x20;

* **SoftwareOne Enterprise Support for AWS** – [SoftwareOne Enterprise Support for AWS](https://docs-aws-essentials.softwareone.cloud/ug/1-0/AWS-Essentials/softwareone-enterprise-support-for-aws), also known as Partner-led support (PLS), provides you with a 15-minute response time SLA. This service is more cost-effective than AWS Business+ and Enterprise support, and has no minimum charge. If you choose this option:
  * SoftwareOne becomes your point of contact for assistance with your AWS resources.&#x20;
  * You receive enterprise-grade AWS support, with added flexibility and partner-driven escalation paths.&#x20;
* **AWS Resold Support** – [AWS Resold Support](https://aws.amazon.com/premiumsupport/aws-resold-support/) allows you to maintain a direct technical relationship with AWS Support. AWS offers multiple [support plans](https://aws.amazon.com/premiumsupport/plans/) to suit different business needs. If you select this option:
  * You contact AWS directly for troubleshooting and operational assistance.&#x20;
  * You must add your support plan to the AWS console's settings.

You can select your preferred support option when placing your order. You can also change your AWS Support plan or transition to SoftwareOne Enterprise Support for AWS at any time during your service term.
