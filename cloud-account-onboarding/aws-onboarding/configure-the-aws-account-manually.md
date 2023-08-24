---
description: >-
  Configure your AWS account so that it's ready for integration with the Client
  Portal.
---

# Configure the AWS Account Manually

{% hint style="warning" %}
**IMPORTANT**: Follow the steps in this topic only if you're instructed to do so by SoftwareOne. Following these steps without assistance from SoftwareOne will result in your AWS account not being fully integrated with the Client Portal.
{% endhint %}

***

### Prerequisites <a href="#before-you-start" id="before-you-start"></a>

Ensure that you have a random external ID in the `pyracloud:aws:extid:{16 random alphanumeric characters}` format. For example, `pyracloud:aws:extid:13kcy2czfja01dfx`. You can create a random string using a [string generator](https://www.random.org/strings/).&#x20;

Once generated, make a note of your external ID. You'll need to share the ID with your SoftwareOne representative.

***

### Executing the CloudFormation Script <a href="#execute-the-pyracloud-cloudformation-script" id="execute-the-pyracloud-cloudformation-script"></a>

**To execute the script**

1. Sign in to the [AWS console](https://aws.amazon.com/console/) as a user with permission to modify IAM resources and execute CloudFormation scripts.
2.  Navigate to CloudFormation.

    1. In the AWS console, select **Services** > **Management & Governance** > **CloudFormation**.
    2. In the upper -right corner of the CloudFormation page, select the region where you wish to execute the CloudFormation script.



    <figure><img src="../../.gitbook/assets/image (51) (1) (1).png" alt=""><figcaption></figcaption></figure>
3. Select **Create stack** and follow these steps:
   1. In **Prerequisite – Prepare template**, select **Template is ready**.
   2. In **Specify template**, select **Amazon S3 URL** and enter the following URL: [https://iepapp0168sda.s3-eu-west-1.amazonaws.com/pyracloud\_onboarding.json](https://iepapp0168sda.s3-eu-west-1.amazonaws.com/pyracloud\_onboarding.json)
4. Select **Next**.

<figure><img src="../../.gitbook/assets/image (52) (1) (1).png" alt=""><figcaption></figcaption></figure>

5. Complete the Specify stack details page as follows:
   1. Enter the name of the stack. The recommended stack name is `PyraCloud-Onboarding`. If you don't use this recommended name, make a note of the name you use and provide it along with the random external ID to SoftwareOne.
   2. Enter the external ID that you generated and the value of the empty GUID as `00000000-0000-0000-0000-000000000000`.
6. Select **Next**.

<figure><img src="../../.gitbook/assets/image (53) (1) (1).png" alt=""><figcaption></figcaption></figure>

7. On the Configure stack options page, no additional settings are required. Select **Next**.

<figure><img src="../../.gitbook/assets/image (54) (1) (1).png" alt=""><figcaption></figcaption></figure>

8. Review the settings associated with the stack and select the **I acknowledge that AWS CloudFormation might create IAM resources with custom names** check box.
9. Select **Create stack**.

After you select **Create stack**, the following page is displayed. To refresh the progress of the stack, select the refresh icon.

<figure><img src="../../.gitbook/assets/image (55) (1) (1).png" alt=""><figcaption></figcaption></figure>

Wait for the status to change to `CREATE_COMPLETE`.

<figure><img src="../../.gitbook/assets/image (56) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Configuring cost and usage reports <a href="#configure-cost-usage-reports" id="configure-cost-usage-reports"></a>

{% hint style="info" %}
**NOTE**: If AWS Organizations is enabled, the following steps are only required in the master account. You don't have to perform these steps for a linked account.
{% endhint %}

If AWS Organizations is not enabled, perform the following steps.

#### Create an S3 Bucket <a href="#create-an-s3-bucket" id="create-an-s3-bucket"></a>

1. In the AWS console, click the **Services** menu item to open the list of services. Under the **Storage** group click the **S3** item.
2. Click **Create bucket**.

<figure><img src="../../.gitbook/assets/image (57) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Complete the **Name and region** page as follows:
   1. In the **Name and region** section, under the **Bucket name** heading, enter a unique name for the bucket. The recommended value for this is `pyracloud.{account number}`. For example, `pyracloud.123456789012`. Make a note of this name to share with SoftwareOne.
   2. In the **Name and region** section, under the **Region** heading, select the region where you want to create the bucket. Make a note of this region to share with SoftwareOne.&#x20;
4. Select **Next**.

<figure><img src="../../.gitbook/assets/image (58) (1) (1).png" alt=""><figcaption></figcaption></figure>

5. On the **Configure options** page, leave the values as default.
6. Select  **Next**.

<figure><img src="../../.gitbook/assets/image (59) (1) (1).png" alt=""><figcaption></figcaption></figure>

7. On the Set Permissions page, leave the values as default.
8. Select **Next**.

<figure><img src="../../.gitbook/assets/image (60) (1) (1).png" alt=""><figcaption></figcaption></figure>

9. On the **Review** page, review the new bucket settings. Select **Create bucket**.

<figure><img src="../../.gitbook/assets/image (61) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

### Creating the cost and usage report <a href="#create-cost-usage-report" id="create-cost-usage-report"></a>

1. In the AWS console, select the account menu item at the top right. Select **My Billing Dashboard**.
2. In the left navigation menu, select **Cost & Usage Reports** and select **Create report**.

<figure><img src="../../.gitbook/assets/image (62) (1).png" alt=""><figcaption></figcaption></figure>

3. Complete the **Report content** page as follows:
   1. Under the **Report name – required** heading, enter a name for the report. The recommended value for this is “PyraCloudCostAndUsage”. Make a note of this name to share with SoftwareONE.
   2. Under the **Additional report details** heading, select the **Include resource IDs** checkbox.
   3. Under the **Data refresh settings** heading, select the **Automatically refresh your Cost & Usage Report when charges are detected for previous months with closed bills** checkbox.
4. Click **Next**.

<figure><img src="../../.gitbook/assets/image (63) (1).png" alt=""><figcaption></figcaption></figure>

4. Complete the **Delivery options** page:
   1. Under the **S3 bucket – required** heading, select **Configure**.
      * On **Step 1 of 2: Configure S3 Bucket**, on the left side, **Select existing bucket** created above from the drop-down. Click **Next**.
      * On **Step 2 of 2: Verify policy**, check the **I have confirmed that this policy is correct** checkbox. Click **Save**.
5. In **Report path prefix**, enter the same value as the Report name field, for example, `PyraCloudCostAndUsage`). This value must be the same as the Report name value.
6. Choose **Time granularity** as **Daily**.
7. Choose **Create new report version**.
8. In **Enable report data integration for**, clear all options.
9. Choose the Compression type as **GZIP**.
10. Select **Next**.

<figure><img src="../../.gitbook/assets/image (64) (1).png" alt=""><figcaption></figcaption></figure>

11. On the **Review** page, review the Cost & Usage Report settings and select **Review and Complete**.

<figure><img src="../../.gitbook/assets/image (65) (1).png" alt=""><figcaption></figcaption></figure>

The report is created.

<figure><img src="../../.gitbook/assets/image (66) (1).png" alt=""><figcaption></figcaption></figure>

***

### Granting access to the S3 Bucket <a href="#grant-pyracloud-access-to-the-s3-bucket" id="grant-pyracloud-access-to-the-s3-bucket"></a>

1. In the AWS console, select **Services** > **Security, Identity, & Compliance** > **IAM**.

<figure><img src="../../.gitbook/assets/image (67) (1).png" alt=""><figcaption></figcaption></figure>

2. Select **Policies.**

<figure><img src="../../.gitbook/assets/image (68) (1).png" alt=""><figcaption></figcaption></figure>

3. Select **Create policy** and then select the **JSON** tab.

<figure><img src="../../.gitbook/assets/image (69) (1).png" alt=""><figcaption></figcaption></figure>

4. Add the following JSON policy. Be sure to replace the `bucketname` with the name of your bucket, for example, `pyracloud.123456789012`. Replace any existing text already in the JSON window.

```json
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

5. Select **Review policy and co**mplete the Review policy page as follows:
   1. Under the **Name** heading, enter a name for the policy. The recommended value is `PyraCloudAllowBillingBucketAccess.`
   2. (Optional) Enter a description.
6. Select **Create policy**.

<figure><img src="../../.gitbook/assets/image (70) (1).png" alt=""><figcaption></figcaption></figure>

***

### **Assigning the policy to the role**

1. Select **Roles** from the navigation menu.

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

2. Choose **PyraCloudRole** from the list of roles.

<figure><img src="../../.gitbook/assets/image (71) (1).png" alt=""><figcaption></figcaption></figure>

3. Select **Attach policies**.&#x20;

<figure><img src="../../.gitbook/assets/image (72) (1).png" alt=""><figcaption></figcaption></figure>

4. Search for the policy created and then select the box next to it. Select **Attach policy**.

<figure><img src="../../.gitbook/assets/image (73) (1).png" alt=""><figcaption></figcaption></figure>

The policy is attached.

<figure><img src="../../.gitbook/assets/image (74) (1).png" alt=""><figcaption></figcaption></figure>

At this point, your AWS account is ready to be integrated with the Client Portal. SoftwareOne will need to perform internal steps to complete the integration.&#x20;

In order to do this, you;ll need to provide the following details to SoftwareOne:

| Detail                            | Example Value                        |
| --------------------------------- | ------------------------------------ |
| AWS Account Number                | 123456789012                         |
| AWS Organizations Enabled?        | Yes                                  |
| AWS Organizations Master Account? | Yes                                  |
| CloudFormation Stack Name         | PyraCloud-Onboarding                 |
| CloudFormation Region             | Ireland (eu-west-1)                  |
| External ID                       | pyracloud:aws:extid:13kcy2czfja01dfx |
| Bucket Name                       | pyracloud.123456789012               |
| Bucket Region                     | Ireland (eu-west-1)                  |
| Report Name                       | PyraCloudCostAndUsage                |
| Report Path Prefix                | PyraCloudCostAndUsage                |

***

### **Enabling your Enterprise Discount Program (EDP) commitment amounts** <a href="#enableyour-enterprise-discount-program-edp-commitment-amounts-in-pyracloud" id="enableyour-enterprise-discount-program-edp-commitment-amounts-in-pyracloud"></a>

If you're taking advantage of AWS’ EDP you can view your commitment amounts in the Client Portal.&#x20;

The portal displays your spending against your commitment so that you can track and plan for upcoming spend. To view your commitment amounts, contact our Support team.

<figure><img src="../../.gitbook/assets/image (75) (1).png" alt=""><figcaption></figcaption></figure>
