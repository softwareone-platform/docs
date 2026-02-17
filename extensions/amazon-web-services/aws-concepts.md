# AWS Terminology and Concepts

This topic covers key concepts and terminology to help you get started with AWS in the SoftwareOne Marketplace.&#x20;

A clear understanding of AWS organizations, account types, billing transfer process, and support models is required to successfully order AWS services from the Marketplace Platform.

### AWS organization

An organization is a collection of AWS accounts that you can manage centrally and organize into a hierarchical, tree-like structure with a main root at the top and organizational units nested under the root.&#x20;

Each account can be placed directly in the root or within one of the organizational units in the hierarchy.

### AWS organizational units

An organizational unit (OU) is a group of AWS accounts within an organization. An OU can also contain other OUs, enabling you to create a hierarchy.

### Account types

When you sign up for Cloud Managed Services for AWS using the Marketplace Platform, you establish a connection between your AWS Organization and a dedicated payer account owned by SoftwareOne.

* **Payer or Management account** - A master payer account plays a crucial role in the AWS organizational structure. It's responsible for consolidating all charges incurred by the linked AWS accounts. This account acts as the central hub to which various linked accounts connect, forming a cohesive AWS organization.
* **Linked account** - These accounts are actively connected to a master payer account. They are responsible for managing specific workloads and utilizing various AWS resources.
* **Standalone account** - A standalone account operates independently of any linked accounts. This type of account is essentially a payer account on its own, provided it has a valid payment method associated with it. AWS requires this to ensure payment processing, so that the account can be billed for the services used. If you are setting up a new AWS account, ensure you have a credit card ready unless you plan to immediately connect it to a master payer account through the **My Organizations** page in the AWS console.

For more information on AWS concepts and account types, see [Terminology and Concepts for AWS Organizations](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_getting-started_concepts.html).

### AWS billing transfer <a href="#aws-billing-transfer" id="aws-billing-transfer"></a>

When you purchase Cloud Managed Services for AWS from SoftwareOne, you connect the management or payer account from your own AWS organization with a management account from SoftwareOne. This process is called AWS billing transfer.

This established connection moves the billing from your AWS account to the SoftwareOne account. While you maintain full access to your own AWS Organization, the billing section for all charges billed by AWS to SoftwareOne is no longer visible.&#x20;

Additionally, any cost and usage report you previously configured is removed and must be reconfigured. For more information on how billing transfer works, see [AWS Billing Transfer](https://aws.amazon.com/aws-cost-management/aws-billing-transfer/).&#x20;

### AWS support levels <a href="#resold-vs-partner-led-aws-support" id="resold-vs-partner-led-aws-support"></a>

When you order AWS services through the SoftwareOne Marketplace, you have two support options. These include **SoftwareOne Enterprise Support for AWS** and **AWS Resold Support**.

You can choose the desired support option when you are placing your order in the SoftwareOne Marketplace. Additionally, you can switch your AWS support plan or transition to SoftwareOne Enterprise support for AWS at any time during your service term.

* **SoftwareOne Enterprise Support for AWS** - [SoftwareOne Enterprise Support for AWS](https://docs-aws-essentials.softwareone.cloud/ug/1-0/AWS-Essentials/softwareone-enterprise-support-for-aws) is also known as Partner-led support (PLS). If you choose this option, SoftwareOne becomes your point of contact for assistance with your AWS resources. This option provides enterprise-grade AWS support without the premium cost, with added flexibility and partner-driven escalation paths. It is validated through the AWS PLS program. With a 15-minute response time SLA, this service is more economical than AWS Business+ and Enterprise support, and there is no minimum charge.
* **AWS Resold Support** - The Resold support is provided directly by AWS. If you select this option, you must contact AWS for troubleshooting and operational assistance. You'll also need to add your support plan to the AWS console's settings. AWS offers several support plans to suit different business needs, such as [AWS Business Support+](https://aws.amazon.com/premiumsupport/plans/business-plus/), [AWS Enterprise Support](https://aws.amazon.com/premiumsupport/plans/enterprise/), and [AWS Unified Operations](https://aws.amazon.com/premiumsupport/plans/unified-operations/). For more information, see [AWS Resold Support](https://aws.amazon.com/premiumsupport/aws-resold-support/).&#x20;
