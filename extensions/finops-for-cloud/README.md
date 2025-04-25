# FinOps for Cloud

FinOps for Cloud is a solution designed to enhance the cloud usage experience by providing detailed insights and management capabilities without actively interfering with processes in your environment.&#x20;

It utilizes billing information, resource state monitoring, and cloud monitoring data to provide actionable recommendations for optimizing cloud resource usage and reducing costs. The platform performs resource discovery using APIs from cloud providers like AWS and Microsoft Azure, ensuring that all resources are accounted for and managed effectively.&#x20;

With FinOps for Cloud, you can explore and analyze your cloud expenses, monitor resource usage, and implement policies to ensure efficient and cost-effective cloud management. The platform's user-friendly interface and robust features empower organizations to achieve greater visibility and control over cloud infrastructure, enabling smarter decision-making and improved financial planning.

## How it works

FinOps for Cloud requires Read-Only rights for the connected cloud account, which serves as the primary data source for all recommendations. The following data is utilized:

* Billing information - all details regarding cloud expenses.
* The state of resources (for actively discoverable types) in the cloud. This is essential for implementing [constraints like TTL, Expense limits](insights/resources/resources-constraint-policies.md), and [Recommendations](insights/recommendations/).
* The monitoring data from the cloud is used to identify underutilized instances.

{% tabs %}
{% tab title="Amazon Web Services (AWS)" %}
The billing information is retrieved from the Data Exports located in a designated S3 bucket in the cloud. See [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) in the AWS documentation to see how it works.

Amazon CloudWatch is the source of monitoring data. For more details, see [Automatic billing data import in AWS](system/data-sources/amazon-web-services/aws-root-account-with-data-export-already-configured.md#automatic-billing-data-import-in-aws).

Resource discovery is done using the Discovery API. For reference, see the following pages in AWS documentation:

* [DescribeInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInstances.html)
* [DescribeVolumes](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeVolumes.html)
* [DescribeSnapshots](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeSnapshots.html)
* [ListBuckets](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html)
{% endtab %}

{% tab title="Microsoft Azure" %}
The billing information is retrieved from the Billing API. See [Usage Details - List](https://learn.microsoft.com/en-us/rest/api/consumption/usage-details/list?view=rest-consumption-2024-08-01\&tabs=HTTP) in Microsoft documentation to see how it works.

Cloud's Monitoring service is used as the source of all monitoring data. For more details, see [Microsoft Azure](system/data-sources/microsoft-azure.md).

Resource discovery is done using Discovery API. For reference, see the following pages in Microsoft documentation:

* [Virtual Machines - List All](https://docs.microsoft.com/en-us/rest/api/compute/virtual-machines/list-all)
* [Disks - List](https://docs.microsoft.com/en-us/rest/api/compute/disks/list)
* [Snapshots - List](https://docs.microsoft.com/en-us/rest/api/compute/snapshots/list)
* [Storage Accounts - List](https://docs.microsoft.com/en-us/rest/api/storagerp/storage-accounts/list)
{% endtab %}

{% tab title="Google Cloud Platform" %}
The billing information is retrieved from the BigQuery service.

Cloud's Monitoring service is used as the source of all monitoring data. For more details, see [Google Cloud Platform](./#google-cloud-platform).

Resource discovery is done using the Discovery API. For reference, see the following pages in Google Cloud documentation:

* [Method: instances.list](https://cloud.google.com/compute/docs/reference/rest/v1/instances/list)
* [Method: disks.list](https://cloud.google.com/compute/docs/reference/rest/v1/disks/list)
* [Method: snapshots.list](https://cloud.google.com/compute/docs/reference/rest/v1/snapshots/list)
* [Buckets: list](https://cloud.google.com/storage/docs/json_api/v1/buckets/list)
* [Method: addresses.list](https://cloud.google.com/compute/docs/reference/rest/v1/addresses/list)
{% endtab %}
{% endtabs %}

## First-time login

When setting up your FinOps for Cloud account, you'll typically receive an invitation email with a link to join your organization's account.&#x20;

Open the invitation email and follow these steps to complete the sign-in process:

1. In your invitation email, select the link to open the FinOps tool.
2. On the sign-up page, enter your first and last name and choose a password for your account.&#x20;
3. Retype the password in the **Confirm password** field and select **Register**. You'll receive a verification code by email.
4. Enter the confirmation code on the sign-in page and select **Confirm**. You'll be signed in to the tool.&#x20;

Use the same credentials to sign in to FinOps for Cloud each time. If you forget your password, use the **Forgot password** option on the sign-in page. We will send you an email with instructions to reset your password.
