---
description: Track your cloud resource usage.
---

# Utilization

The **Utilization** module allows you to track your cloud resource usage so you can determine which resources can be de-allocated or resized.

You can access the Utilization module by navigating to the main menu of the Client Portal and selecting **Cloud tools > Utilization**.&#x20;

## Utilization page

The **Utilization** page contains search filters and tabs that allow you to choose a resource type. When you search for a resource, your list of resources are displayed in the grid.&#x20;

<figure><img src="../../.gitbook/assets/image (802).png" alt=""><figcaption></figcaption></figure>

1. **Search filters** - You can search by relevant resource properties and additionally, you can filter resources by recommendations (if applicable). For example, you can review all resources recommended for “shutdown” and see if utilization is low.
2. **Virtual Machine and Storage tabs** - Utilization currently supports two resource types, Virtual Machines (that include Azure scale sets) and Storage accounts. Utilization supports both Azure and Amazon resources in one single unified view.
3. **List of resources** - On the main page you will see a table with a list of your cloud resources with the main metric selected – for Virtual Machines it is _Average CPU_, and for Storage Accounts it is _Capacity_. The table can be sorted by “all visible columns” so you can optimize your analysis.

## Utilization details page

You can navigate to details by clicking **View** on the **Utilization** page.

<figure><img src="../../.gitbook/assets/image (803).png" alt=""><figcaption></figcaption></figure>

The page contains four main areas:

1. **Resource Basic Information** - This section contains information, such as group, subscription, provider, and tags. Additionally, you can navigate directly to the Recommendation module.
2. **Date Range Selector** - Currently, there are two types of selectors – 30 days and 7 days (older data is automatically removed). In “30 days” mode you see a daily aggregation chart (4) and in the 7 days chart you see hourly aggregation.
3. **Metric Selector** - This drop-down allows you to view available metrics. The module currently supports CPU and network traffic for Virtual Machines, and Capacity and Counters for storage accounts. After selecting, the metric chart is adjusted automatically.
4. **Chart Area** - As well as plotting metrics data, the chart can also present scale set resources, so you can analyze multiple nodes running on scale set.

<figure><img src="../../.gitbook/assets/image (805).png" alt=""><figcaption></figcaption></figure>

By clicking on the legend (1) you can show/hide scale set nodes.

## Configuring alerts <a href="#configuring-alerts" id="configuring-alerts"></a>

The utilization module supports custom alerts, so you can set up notifications based on the low utilization of your machines, or overutilization of your storage accounts.

<figure><img src="../../.gitbook/assets/image (808).png" alt=""><figcaption></figcaption></figure>

To create alerts, complete your search and then select **Create Alert**.

<figure><img src="../../.gitbook/assets/image (809).png" alt=""><figcaption></figcaption></figure>

By default, the alert modal appears with Virtual Machine (CPU) notifications. You can configure notifications to be alerted if machine utilization (from your search criteria) drops below (10%, 20%, or a custom percentage).

<figure><img src="../../.gitbook/assets/image (810).png" alt=""><figcaption></figcaption></figure>

You can also configure alerts based on the capacity of the storage accounts. If it grows above a defined threshold you will then be notified. The alerts are generated once per day at 5:00 a.m. UTC

## Configuring AWS access <a href="#configuring-aws-access" id="configuring-aws-access"></a>

If the utilization module is not able to pull utilization metrics, you will see the following message:

<figure><img src="../../.gitbook/assets/image (807).png" alt=""><figcaption></figcaption></figure>

Utilization uses CloudWatch to pull metrics. If you see the above message, it means CloudWatch was not assigned to **PyraCloudRole**.&#x20;

Follow these steps to resolve this issue:

1. Open the AWS Console and navigate to IAM.

<figure><img src="../../.gitbook/assets/image (811).png" alt=""><figcaption></figcaption></figure>

2. Locate **PyraCloudRole**.

<figure><img src="../../.gitbook/assets/image (813).png" alt=""><figcaption></figcaption></figure>



3. In the role, click **PyraCloud ReadOnlyPolicy**.

<figure><img src="../../.gitbook/assets/image (814).png" alt=""><figcaption></figcaption></figure>

4. Click **Edit policy**.

<figure><img src="../../.gitbook/assets/image (815).png" alt=""><figcaption></figcaption></figure>

5. Switch to **JSON** view.

<figure><img src="../../.gitbook/assets/image (816).png" alt=""><figcaption></figcaption></figure>

6. In the editor, add `cloudwatch:GetMetricStatistics` and click **Review.**

<figure><img src="../../.gitbook/assets/image (817).png" alt=""><figcaption></figcaption></figure>

7. In the review summary, you should see CloudWatch permission.

<figure><img src="../../.gitbook/assets/image (818).png" alt=""><figcaption></figcaption></figure>

8. Save your changes.

If using AWS Organizations, repeat these steps for all linked accounts. Utilization synchronizes data every hour, so your utilization metrics will be synchronized with the Client Portal during the next sync.
