# AWS Organizations requirements

This topic describes how to prepare an AWS account for onboarding with SoftwareOne.&#x20;

It describes how to enable AWS Organizations, required organizational services, and settings needed to support secure onboarding and governance.

### Enable AWS Organizations

AWS Organizations is required to onboard Essentials and manage organization-wide services.

To enable AWS Organizations:&#x20;

1. Sign in to the AWS Management Console.
2. Open **AWS Organizations**.
3. Choose **Create an organization**.
4. Select **Enable all features**.

{% hint style="info" %}
* All features must be enabled.
* The account used to create the organization becomes the AWS Organizations management account.
* After enabling all features, this setting cannot be reverted.
{% endhint %}

### Enable required organizational services

The following services must be enabled at the AWS Organizations level to support secure and automated onboarding.&#x20;

This is done from the organization management account and only needs to be completed once.

#### Enable Service Control Policies (SCPs)

SCPs allow organization-wide governance controls to be applied across AWS accounts. To enable SCPs:

1. Open **AWS Organizations**.
2. Select **Policies**.
3. Verify that **Service control policies** are enabled.
4. If SCPs are disabled, choose **Enable**.

No policies need to be created or attached at this stage.

#### Enable CloudTrail as an Organizational Service

Enabling CloudTrail as an organizational service allows the organization to manage organization-level CloudTrail configurations when required by services such as Landing Zones.

Enabling this setting does not create or configure any CloudTrail trails.&#x20;

1. Open **AWS Organizations**.
2. Select **Services**.
3. Locate **AWS CloudTrail**.
4. Verify that CloudTrail is enabled for the organization.

No CloudTrail trails need to be created manually.

#### Enable CloudFormation StackSets

CloudFormation StackSets must be enabled both in AWS Organizations and in the\
CloudFormation console. Those are required to complete SoftwareOne onboarding.

**Enable StackSets in AWS Organizations**

1. Open **AWS Organizations**.
2. Select **Services**.
3. Locate **AWS CloudFormation StackSets**.
4. Verify that StackSets is enabled for the organization.

**Enable StackSets in AWS CloudFormation**

1. Open **AWS CloudFormation**.
2. Select **StackSets** from the navigation menu.
3. If prompted, enable StackSets.
4. Verify that service-managed permissions are available.

You do not need to create any StackSets manually.

### Activate billing access for IAM users and roles

IAM users and roles cannot access AWS Billing and Cost Management by default. Billing access must be enabled to allow delegated users and roles to view billing information.

1. In the AWS Management Console, open **Account settings** or use the account menu in the   \
   top-right corner and select **Account**.
2. Scroll to **IAM user and role access to Billing information**.
3. Select **Edit**.
4. Enable **Activate IAM Access**.
5. Choose **Update**.

{% hint style="info" %}
Activating IAM access alone doesn't grant the roles the necessary permissions for these\
Billing and Cost Management console pages. In addition to activating IAM access, you\
must also attach the required IAM policies to those roles.
{% endhint %}

### Next steps

After completing these requirements, return to the SoftwareOne Marketplace purchase flow and provide your AWS Organizations management account ID to continue onboarding.
