---
description: Manage your AWS recommendations.
---

# AWS recommendations

AWS recommendations are divided into the following categories:

* **Savings** - These recommendations can enable cost savings.
* **Security** - These recommendations can help improve the security of an AWS environment.
* **High Availability** - These recommendations can help to improve the availability of an AWS environment.
* **Performance** - These recommendations can help improve the performance of an AWS environment.

## AWS recommendation sources <a href="#aws-recommendation-sync-sources" id="aws-recommendation-sync-sources"></a>

The Client Portal downloads AWS recommendations from [AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/) and [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/).

### AWS Trusted Advisor

AWS Trusted Advisor is available in any environment configured with the correct AWS [support plan](https://aws.amazon.com/premiumsupport/plans/). AWS Trusted Advisor provides information for various recommendation categories, for example, Savings, Security, Performance, High Availability, and Service Limits. Recommendations are fetched from the AWS Trusted Advisor if:

* AWS Business or Enterprise support plan is enabled for an account within AWS.&#x20;
* Correct permissions are enabled for AWS accounts in the Client Portal. For information on permissions required to download recommendations from AWS Trusted Advisor, see [Reonboarding AWS Recommendations](../cloud-tenant-setup/aws-onboarding/update-aws-account-permissions.md#re-onboard-aws-recommendations).

### AWS Cost Explorer <a href="#aws-cost-explorer" id="aws-cost-explorer"></a>

AWS Cost Explorer is available to any environment with the Cost Explorer enabled in AWS. The Client Portal can fetch Reservation-based recommendations from the Cost Explorer. These reservation-based recommendations are Reserved Instance (RI) purchase recommendations that could help you reduce costs. Recommendations can be fetched from the AWS Cost Explorer if:

1. [Cost Explorer is enabled in AWS](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-enable.html).
2. Cost Explorer is enabled for your AWS Account through the **Cloud Tenant Setup** module in the Client Portal. The Cost Explorer is enabled by default.

By default, all AWS accounts are configured to pull recommendations from AWS Cost Explorer.

## Synchronization information

The synchronization with AWS Cost Explorer occurs once a week (as opposed to all recommendations-related synchronization processes that run once an hour). This schedule is not configurable. This is so we can minimize costs, as fetching data from Cost Explorer is chargeable.&#x20;

AWS charges 0.05 USD per account for every sync. The Client Portal will sync recommendation data per account once a week. When Cost Explorer is turned on (within AWS and the Client Portal), the amount should be a maximum of 0.20 USD per AWS account per month.

To effectively utilize these recommendations, make sure that AWS Cost Explorer is turned on within AWS for each of your accounts. See [Enabling Cost Explorer](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ce-enable.html) to turn on Cost Explorer within AWS.

If you're facing synchronization issues, see [How to resolve AWS recommendation synchronization errors](../../../help-and-support/frequently-asked-questions/how-to-resolve-aws-recommendation-synchronization-errors.md).&#x20;

## Disable AWS Cost Explorer recommendations

Cost Explorer recommendations provide reserved instance purchase recommendations for Amazon EC2, Redshift, and RDS. Turning off these recommendations will mean that you won't have access to these savings-based recommendations.

You can turn off Cost Explorer at the AWS account level. There is no option to turn Cost Explorer for all AWS accounts in one go. See [Syncing AWS Cost Explorer recommendations](../cloud-tenant-setup/aws-onboarding/activate-an-aws-account.md#sync-aws-cost-explorer-recommendations) to disable AWS Cost Explorer Recommendations for your AWS account.

## Related topics

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

{% content-ref url="view-recommendations.md" %}
[view-recommendations.md](view-recommendations.md)
{% endcontent-ref %}

{% content-ref url="manage-recommendations.md" %}
[manage-recommendations.md](manage-recommendations.md)
{% endcontent-ref %}

{% content-ref url="azure-recommendations.md" %}
[azure-recommendations.md](azure-recommendations.md)
{% endcontent-ref %}

{% content-ref url="office-365-recommendations.md" %}
[office-365-recommendations.md](office-365-recommendations.md)
{% endcontent-ref %}
