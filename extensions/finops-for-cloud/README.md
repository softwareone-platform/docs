# FinOps for Cloud

## Overview <a href="#about-optscale" id="about-optscale"></a>

To be added

## How it works <a href="#amazon-web-services-aws" id="amazon-web-services-aws"></a>

FinOps for Cloud is focused on enhancing to improving the cloud usage experience without actively interfering with processes in your environment.&#x20;

It requires **Read-Only** rights for the connected cloud account, which serves as the primary Data Source for all recommendations. The following data is utilized:

* Billing information - all details regarding cloud expenses.
* The state of resources (for actively discoverable types) in the cloud. This is essential for implementing Constraints like TTL and Expense limits, as well as for Recommendations.
* Monitoring data from the cloud is used to identify underutilized instances.

{% tabs %}
{% tab title="Amazon Web Services (AWS)" %}
The billing information is retrieved from the Data Exports located in a designated S3 bucket in the cloud. See [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) in AWS documentation.

Amazon Cloud Watch is used as the source of monitoring data. For details, see [Automatic billing data import in AWS](data-sources/amazon-web-services/aws-root-account-with-data-export-already-configured.md#automatic-billing-data-import-in-aws).

Resource discovery is done using the Discovery API. See the following pages in AWS documentation to learn more:

* [DescribeInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInstances.html)
* [DescribeVolumes](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeVolumes.html)
* [DescribeSnapshots](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeSnapshots.html)
* [ListBuckets](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html)
{% endtab %}

{% tab title="Microsoft Azure" %}
The billing information is retrieved through the Billing API. See [Usage Details - List](https://learn.microsoft.com/en-us/rest/api/consumption/usage-details/list?view=rest-consumption-2024-08-01\&tabs=HTTP) in Microsoft documentation.

Cloud's Monitoring service is used as the source of all monitoring data. For more details, see [Microsoft Azure](data-sources/microsoft-azure.md).

Resource discovery is done using Discovery API. See the following pages in Microsoft documentation to learn more:

* [Virtual Machines - List All](https://docs.microsoft.com/en-us/rest/api/compute/virtual-machines/list-all)
* [Disks - List](https://docs.microsoft.com/en-us/rest/api/compute/disks/list)
* [Snapshots - List](https://docs.microsoft.com/en-us/rest/api/compute/snapshots/list)
* [Storage Accounts - List](https://docs.microsoft.com/en-us/rest/api/storagerp/storage-accounts/list)
{% endtab %}

{% tab title="Google Cloud Platform" %}
The billing information is retrieved from the BigQuery service.

Cloud's Monitoring service is used as the source of all monitoring data. For more details, see [Google Cloud Platform](./#google-cloud-platform).

Resource discovery is done using the Discovery API. See the following pages in Google Cloud documentation to learn more:

* [Method: instances.list](https://cloud.google.com/compute/docs/reference/rest/v1/instances/list)
* [Method: disks.list](https://cloud.google.com/compute/docs/reference/rest/v1/disks/list)
* [Method: snapshots.list](https://cloud.google.com/compute/docs/reference/rest/v1/snapshots/list)
* [Buckets: list](https://cloud.google.com/storage/docs/json_api/v1/buckets/list)
* [Method: addresses.list](https://cloud.google.com/compute/docs/reference/rest/v1/addresses/list)
{% endtab %}
{% endtabs %}
