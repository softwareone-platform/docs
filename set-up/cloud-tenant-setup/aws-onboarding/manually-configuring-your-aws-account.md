---
description: >-
  Configure your AWS account so that it's ready for integration with the Client
  Portal.
---

# Manually configuring your AWS account

{% hint style="info" %}
**NOTE**: Follow this topic only if instructed to do so by SoftwareOne. Following these steps without assistance from SoftwareOne will not result in your AWS account being fully integrated with PyraCloud.
{% endhint %}

***

### Prerequisites <a href="#before-you-start" id="before-you-start"></a>

You must have a random external ID. The ID must be in the`pyracloud:aws:extid:{16 random alphanumeric characters}` format. For example, `pyracloud:aws:extid:13kcy2czfja01dfx`. You can create the random string yourself using a [string generator](https://www.random.org/strings/).&#x20;

Once generated, make a note of your external ID. You'll need to share the ID with your SoftwareOne representative for integration with PyraCloud.

***

### Executing the CloudFormation Script <a href="#execute-the-pyracloud-cloudformation-script" id="execute-the-pyracloud-cloudformation-script"></a>

**To execute the script**

1. Sign in to the [AWS console](https://aws.amazon.com/console/) as a user with permission to modify IAM resources and execute CloudFormation scripts.
2. Navigate to CloudFormation.
   1. In the AWS console, select **Services** > **Management & Governance** > **CloudFormation**.
   2. At the top-right of the CloudFormation Screen, select the region you wish to execute the CloudFormation script in.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-4-1024x622.png" alt=""><figcaption></figcaption></figure>

3. Select **Create stack** and follow these steps:
   1. In **Prerequisite – Prepare template**, select **Template is ready**.
   2. In **Specify template**, select **Amazon S3 URL** and enter the following URL: [https://iepapp0168sda.s3-eu-west-1.amazonaws.com/pyracloud\_onboarding.json](https://iepapp0168sda.s3-eu-west-1.amazonaws.com/pyracloud\_onboarding.json)
4. Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-5-1024x622.png" alt=""><figcaption></figcaption></figure>

5. Complete the Specify stack details page as follows:
   1. Enter the name of the stack. The recommended stack name is PyraCloud-Onboarding. If you do not use this recommended name, make a note of the name you use and provide it along with the random external ID to SoftwareOne.
   2. Enter the external ID that you generated, the empty GUID value as 00000000-0000-0000-0000-000000000000.
6. Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-6-1024x622.png" alt=""><figcaption></figcaption></figure>

7. On the Configure stack options page, no additional settings are required. Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-7-1024x803.png" alt=""><figcaption></figcaption></figure>

8. Review the settings associated with the stack and select the **I acknowledge that AWS CloudFormation might create IAM resources with custom names** check box.
9. Select **Create stack**.

After you select **Create stack**, the following page is displayed. To refresh the progress of the stack, select the refresh icon.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-9-1024x622.png" alt=""><figcaption></figcaption></figure>

Wait for the status to change to CREATE\_COMPLETE.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-11-1024x622.png" alt=""><figcaption></figcaption></figure>

***

### Configuring cost and usage reports <a href="#configure-cost-usage-reports" id="configure-cost-usage-reports"></a>

{% hint style="info" %}
**NOTE**: If AWS Organizations is enabled, the following steps are only required in the master account. There is no need to perform these steps for a linked account.
{% endhint %}

If you do not have AWS Organizations enabled, then you should perform the following steps.

#### Create an S3 Bucket <a href="#create-an-s3-bucket" id="create-an-s3-bucket"></a>

In the AWS console, click the **Services** menu item to open the list of services. Under the **Storage** group click the **S3** item.

Click **Create bucket**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-12-1024x622.png" alt=""><figcaption></figcaption></figure>

Complete the **Name and region** page as follows:

1. In the **Name and region** section, under the **Bucket name** heading, enter a unique name for the bucket. The recommended value for this is “pyracloud.{account number}”. For example, “pyracloud.123456789012”. Make a note of this name to share with SoftwareONE.
2. In the **Name and region** section, under the **Region** heading, select the region to create the bucket in. Make a note of this region to share with SoftwareONE.

Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-13-1024x622.png" alt=""><figcaption><p><strong>Figure 11: S3 Bucket, name and region</strong></p></figcaption></figure>

On the **Configure options** page, leave the values as default.

Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-14-1024x622.png" alt=""><figcaption><p><strong>Figure 12: S3 Bucket, configure options</strong></p></figcaption></figure>

On the Set permissions page, leave the values as default.

Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-15-1024x622.png" alt=""><figcaption><p><strong>Figure 13: S3 Bucket, set permissions</strong></p></figcaption></figure>

On the **Review** page, review the new bucket settings.

Click **Create bucket**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-16-1024x622.png" alt=""><figcaption><p><strong>Figure 14: S3 Bucket, review</strong></p></figcaption></figure>

#### Create Cost & Usage Report <a href="#create-cost-usage-report" id="create-cost-usage-report"></a>

In the AWS console, click the account menu item at the top right.

Click **My Billing Dashboard**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-17-1024x622.png" alt=""><figcaption></figcaption></figure>

In the left navigation menu, click **Cost & Usage Reports**.

Click **Create report**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-18-1024x622.png" alt=""><figcaption></figcaption></figure>

Complete the **Report content** page as follows:

1. Under the **Report name – required** heading, enter a name for the report. The recommended value for this is “PyraCloudCostAndUsage”. Make a note of this name to share with SoftwareONE.
2. Under the **Additional report details** heading, check the **Include resource IDs** checkbox.
3. Under the **Data refresh settings** heading, check the **Automatically refresh your Cost & Usage Report when charges are detected for previous months with closed bills** checkbox.

Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-19-1024x622.png" alt=""><figcaption></figcaption></figure>

Complete the **Delivery options** page as follows:

1. Under the **S3 bucket – required** heading, click **Configure**.
   1. On **Step 1 of 2: Configure S3 Bucket**, on the left side, **Select existing bucket** created above from the drop-down. Click **Next**.
   2. On **Step 2 of 2: Verify policy**, check the **I have confirmed that this policy is correct** checkbox. Click **Save**.
2. Under the **Report path prefix** heading, enter the same value as the Report name field (e.g. “PyraCloudCostAndUsage”). **Note**: this value MUST be the same as the Report name value.
3. Under the **Time granularity** heading, select **Daily**.
4. Under the **Report versioning** heading, select **Create new report version**.
5. Under the **Enable report data integration for** heading, deselect all options.
6. Under the **Compression type** heading, select **GZIP**.

Click **Next**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-20-1024x622.png" alt=""><figcaption></figcaption></figure>

On the **Review** page, review the Cost & Usage Report settings.

Click **Review and Complete**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-21-1024x622.png" alt=""><figcaption></figcaption></figure>

The report is created.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-22-1024x622.png" alt=""><figcaption></figcaption></figure>

#### Grant PyraCloud Access to the S3 Bucket <a href="#grant-pyracloud-access-to-the-s3-bucket" id="grant-pyracloud-access-to-the-s3-bucket"></a>

**Create a Policy**

In the AWS console, click the **Services** menu item to open the list of services. Under the **Security, Identity, & Compliance** group click the **IAM** item.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-23-1024x622.png" alt=""><figcaption></figcaption></figure>

Click **Policies** in the left hand navigation menu.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-24-1024x622.png" alt=""><figcaption></figcaption></figure>

Click **Create policy** then click the **JSON** tab.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-25-1024x622.png" alt=""><figcaption></figcaption></figure>

Paste the following JSON policy into the window. Be sure to replace the _bucketname_ values with the real name of your bucket (e.g. “pyracloud.123456789012” in the examples above). Replace any existing text already in the JSON window.

Click **Review policy**.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowPyraCloudToAccessBillingBucket",
            "Effect": "Allow",
            "Action": [
                "s3:GetObject",
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:s3:::bucketname",
                "arn:aws:s3:::bucketname/*"
            ]
        },
        {
            "Sid": "AllowPyraCloudToListAllBuckets",
            "Effect": "Allow",
            "Action": [
                "s3:ListAllMyBuckets",
                "s3:HeadBucket"
            ],
            "Resource": "*"
        }
    ]
}
```

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-26-1024x622.png" alt=""><figcaption></figcaption></figure>

Complete the Review policy page as follows:

1. Under the **Name** heading, enter a name for the policy. The recommended value is “PyraCloudAllowBillingBucketAccess”.
2. Under the **Description** field, enter a description. This can be left blank.

Click **Create policy**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-28-1024x622.png" alt=""><figcaption></figcaption></figure>

**Assign the Policy to the PyraCloud Role**

Click **Roles** in the left hand navigation menu.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-29-1024x622.png" alt=""><figcaption></figcaption></figure>

Click the **PyraCloudRole** role in the list on the right.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-31-1024x622.png" alt=""><figcaption></figcaption></figure>

Click **Attach policies**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-32-1024x622.png" alt=""><figcaption></figcaption></figure>

Search for the policy created above and check the box next to it.

Click **Attach policy**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-33-1024x622.png" alt=""><figcaption></figcaption></figure>

The policy is attached.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/image-34-1024x622.png" alt=""><figcaption></figcaption></figure>

At this point, your AWS account is ready to be integrated with PyraCloud. SoftwareONE will need to perform some steps internally to complete this. In order to do this, you will need to provide the following details to SoftwareONE:

| **Detail**                        | **Example Value**                    |
| --------------------------------- | ------------------------------------ |
| AWS Account Number                | 123456789012                         |
| AWS Organizations Enabled?        | Yes                                  |
| AWS Organizations Master Account? | Yes                                  |
|                                   |                                      |
| CloudFormation Stack Name         | PyraCloud-Onboarding                 |
| CloudFormation Region             | Ireland (eu-west-1)                  |
|                                   |                                      |
| External ID                       | pyracloud:aws:extid:13kcy2czfja01dfx |
|                                   |                                      |
| Bucket Name                       | pyracloud.123456789012               |
| Bucket Region                     | Ireland (eu-west-1)                  |
|                                   |                                      |
| Report Name                       | PyraCloudCostAndUsage                |
| Report Path Prefix                | PyraCloudCostAndUsage                |

***

### **Enabling your Enterprise Discount Program (EDP) commitment amounts in PyraCloud** <a href="#enableyour-enterprise-discount-program-edp-commitment-amounts-in-pyracloud" id="enableyour-enterprise-discount-program-edp-commitment-amounts-in-pyracloud"></a>

If you are taking advantage of AWS’ EDP you can view your commitment amounts in PyraCloud. PyraCloud will show you how you are spending against your commitment so that you can track and plan for upcoming spend. Please reach out to our [support team](mailto:support@pyracloud.com) to get setup today.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2020/02/EDP-AWS-Image-1.jpg" alt="" height="570" width="774"><figcaption></figcaption></figure>
