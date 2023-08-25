# How to turn off Cost Explorer recommendations

Cost Explorer recommendations provide reserved instance purchase recommendations for Amazon EC2, Redshift, and RDS. Turning off these recommendations will mean that you don't have access to these savings-based recommendations.

You can turn off Cost Explorer at the AWS account level. There is no option to turn Cost Explorer for all AWS accounts in one go. See [Syncing AWS Cost Explorer recommendations](../../cloud-account-onboarding/aws-onboarding/activate-an-aws-account.md#sync-aws-cost-explorer-recommendations) to turn off AWS Cost Explorer Recommendations for your AWS account.

***

### Troubleshooting synchronization with AWS Trusted Advisor and AWS Cost Explorer

**AWS Trusted Advisor or Cost Explorer is not correctly configured for at least one AWS account.**

If PyraCloud is not able to download recommendations, the information is reflected in the health check for AWS accounts on the main page.&#x20;

The following image shows the AWS synchronization error:

<figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

To resolve the error:

1. Select **Fix**.&#x20;
2. On the Synchronization Information page, review the synchronization information.&#x20;

<figure><img src="../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

The following are the possible issues and their description:

| Issue                                                                    | Description                                                                                          |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| Cannot read recommendations from AWS Trusted Advisor                     | It means that PyraCloud doesn't have the right permission to pull data from AWS Trusted Advisor.     |
| Cannot read recommendations from AWS Cost Explorer                       | It means that PyraCloud doesn't have the right permission to pull data from AWS Cost Explorer.       |
| Cannot read recommendations from AWS Trusted Advisor due to support plan | It means that the AWS account has low support to download data through API for Trusted Advisor.      |
| AWS Cost Explorer disabled in PyraCloud                                  | It means that synchronization of recommendations from AWS Cost Explorer is not enabled in PyraCloud. |
| AWS Cost Explorer disabled in AWS                                        | It means that AWS Cost Explorer was not enabled within the AWS account.                              |

If you've enabled the Cost Explorer and AWS permissions, but PyraCloud is still showing an error, ensure that the Amazon EC2 rightsizing recommendations are enabled. For information on how to enable rightsizing recommendations, see [Optimizing your cost with Rightsizing Recommendations](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-rightsizing.html) in AWS documentation.

#### **AWS Trusted Advisor and AWS Cost Explorer both show a green check on the overview Page**

<figure><img src="../../.gitbook/assets/image (166).png" alt=""><figcaption></figcaption></figure>

If the green check is displayed, it means that for all AWS accounts, PyraCloud is able to download recommendations from the AWS Trusted Advisor and AWS Cost Explorer.
