# How do I resolve AWS recommendation errors?

The Client Portal downloads AWS recommendations from [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/) and [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/).&#x20;

If the Client Portal is unable to download recommendations, a message is displayed in the health check for the AWS accounts on the Cloud Cost Optimization page.&#x20;

The following image shows the AWS synchronization error:

<figure><img src="../../.gitbook/assets/image (780).png" alt=""><figcaption></figcaption></figure>

This error means that the AWS Trusted Advisor or Cost Explorer is not configured correctly for at least one AWS accoun&#x74;**.**&#x20;

To resolve this issue:

1. Select **Fix**.&#x20;
2. On the Synchronization Information page, review the details and follow the solution to resolve the error.&#x20;

<figure><img src="../../.gitbook/assets/image (678).png" alt=""><figcaption></figcaption></figure>

The following are the possible issues and their description:

| Issue                                                                    | Description                                                                                                      |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------- |
| Cannot read recommendations from AWS Trusted Advisor                     | It means that the Client Portal doesn't have the right permission to pull data from AWS Trusted Advisor.         |
| Cannot read recommendations from AWS Cost Explorer                       | It means that Client Portal doesn't have the right permission to pull data from AWS Cost Explorer.               |
| Cannot read recommendations from AWS Trusted Advisor due to support plan | It means that the AWS account has low support to download data through API for Trusted Advisor.                  |
| AWS Cost Explorer disabled in the Client Portal                          | It means that the synchronization of recommendations from AWS Cost Explorer is not enabled in the Client Portal. |
| AWS Cost Explorer disabled in AWS                                        | It means that AWS Cost Explorer is not enabled in the AWS account.                                               |

If you've enabled the Cost Explorer and AWS permissions, but the Client Portal is still showing an error, ensure that the Amazon EC2 rightsizing recommendations are enabled. For information on how to enable rightsizing recommendations, see [Optimizing your cost with Rightsizing Recommendations](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-rightsizing.html) in AWS documentation.
