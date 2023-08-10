---
description: Follow these steps to turn off the Cost Explorer recommendations.
---

# How to turn off the Cost Explorer recommendations

Cost Explorer recommendations provide reserved instance purchase recommendations for Amazon EC2, Redshift, and RDS. Turning off these recommendations will mean that you don't have access to these savings-based recommendations.

You can turn off Cost Explorer at an AWS account level. There is no option to turn Cost Explorer for all AWS accounts in one go. See [Activating your AWS Account](../../set-up/cloud-tenant-setup/aws-onboarding/activating-your-aws-account.md) to turn off AWS Cost Explorer Recommendations for your AWS account.

***

### Troubleshooting Synchronization with AWS Trusted Advisor and AWS Cost Explorer

#### **AWS Trusted Advisor and AWS Cost Explorer both show a green tick on the overview Page**

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

* It means that for all AWS accounts, we are able to download recommendations from AWS Trusted Advisor
* It means that for all AWS accounts, we are able to download recommendations from AWS Cost Explorer.

#### **AWS Trusted Advisor or Cost Explorer is not correctly configured for at least one AWS account.**

When for at least one AWS account, PyraCloud is not able to download recommendations, the information is reflected in the health check for AWS accounts on the main page.

<figure><img src="../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

Selecting **Fix** opens up the details page.

<figure><img src="../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

Possible issues and their description:

| Issue                                                                    | Description                                                                                              |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| Cannot read recommendations from AWS Trusted Advisor                     | It means that PyraCloud doesn't have the right permission to pull data from AWS Trusted Advisor.         |
| Cannot read recommendations from AWS Cost Explorer                       | It means that PyraCloud doesn't have the right permission to pull data from AWS Cost Explorer.           |
| Cannot read recommendations from AWS Trusted Advisor due to support plan | It means that the AWS account has low support to download data through API for Trusted Advisor.          |
| AWS Cost Explorer disabled in PyraCloud                                  | It means that synchronization of recommendations from AWS Cost Explorer is not enabled within PyraCloud. |
| AWS Cost Explorer disabled in AWS                                        | It means that AWS Cost Explorer was not enabled within the AWS account.                                  |
