---
description: >-
  Track your cloud resource usage so you can determine which resources can be
  de-allocated or resized.
---

# Cloud Utilization

***

### Accessing Utilization

**To access the Utilization module**

* From the main menu, navigate to **Analyze** and select **Utilization.**

The Utilization page contains the following  sections:

<figure><img src="../../.gitbook/assets/image (238).png" alt=""><figcaption></figcaption></figure>

* Search Bar: You can search by relevant resource properties and additionally, you can filter resources by recommendations (if applicable). For example, you can review all resources recommended for “shutdown” and see if utilization is low.
* Resource types selector: Utilization currently supports two resource types, Virtual Machines (that include Azure scale sets) and Storage accounts. Utilization supports both Azure and Amazon resources in one single unified view.
* List of resources: On the main page you will see a table with a list of your cloud resources with the main metric selected – for Virtual Machines it is _Average CPU_, and for Storage Accounts it is _Capacity_. The table can be sorted by “all visible columns” so you can optimize your analysis.

***

### Resource details <a href="#resource-details" id="resource-details"></a>

The core feature of utilization is plotting metrics. You can navigate to details by clicking “View” on the list.

<figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure>

The page contains four main areas:

1. Resource Basic Information: This section contains information like group, subscription, provider, and tags. Additionally, you can navigate directly to [recommendation ](https://help.pyracloud.com/knowledge-base/recommendations/)or [resource ](https://help.pyracloud.com/knowledge-base/managing-tags-and-resources/)modules.
2. Date Range Selector: Currently, there are two types of selectors – 30 days and 7 days (older data is automatically removed). In “30 days” mode you see a daily aggregation chart (4) and in “7 days” chart you see hourly aggregation.
3. Metric Selector: This drop-down allows you to view available metrics. The module currently supports CPU and network traffic for Virtual Machines, and Capacity and Counters for storage accounts. After selecting, the metric chart is adjusted automatically.
4. Chart Area: As well as plotting metrics data, the chart can also present scale set resources, so you can analyze multiple nodes running on scale set.

<figure><img src="../../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>

By clicking on the legend (1) you can show/hide scale set nodes.

***

### Configuring alerts <a href="#configuring-alerts" id="configuring-alerts"></a>

The utilization module supports custom alerts, so you can set up notifications based on the low utilization of your machines, or overutilization of your storage accounts.

<figure><img src="../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

To create alerts, complete your search and then select **Create Alert**.

<figure><img src="../../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

By default, the alert modal appears with Virtual Machine (CPU) notifications. You can configure notifications to be alerted if machine utilization (from your search criteria) drops below (10%, 20%, or a custom percentage).

<figure><img src="../../.gitbook/assets/image (246).png" alt=""><figcaption></figcaption></figure>

You can also configure alerts based on the capacity of the storage accounts. If it grows above a defined threshold you will then be notified. The alerts are generated once per day at 5:00 a.m. UTC

***

### Configuring AWS Access <a href="#configuring-aws-access" id="configuring-aws-access"></a>

If the utilization module is not able to pull utilization metrics, you will see the below popup message:

<figure><img src="../../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

Utilization uses CloudWatch to pull metrics. If you see the above message, it means CloudWatch was not assigned to **PyraCloudRole**.

To fix this:

1. Open the AWS Console and navigate to IAM.

<figure><img src="../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>

2. Locate PyraCloudRole:

<figure><img src="../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>



3. In the role, open PyraCloud ReadOnlyPolicy.

<figure><img src="../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

4. Select **Edit policy**.

<figure><img src="../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

5. Switch to JSON view.

<figure><img src="../../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

6. In the editor, add `cloudwatch:GetMetricStatistics` and select **Review.**

<figure><img src="../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>

7. In the review summary, you should see CloudWatch permission.

<figure><img src="../../.gitbook/assets/image (254).png" alt=""><figcaption></figcaption></figure>

8. Select **Save Changes**.

If you are using AWS Organizations, repeat these steps for all linked accounts.

Utilization synchronizes data every hour, so your utilization metrics will be synchronized with PyraCloud during the next sync.
