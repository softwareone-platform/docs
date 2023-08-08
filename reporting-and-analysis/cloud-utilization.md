# Cloud Utilization

PyraCloud Utilization helps you track usage of your cloud resources. This enables you to determine whether certain resource need to be de-allocated or resized.

### Exploring Utilization <a href="#exploring-utilization" id="exploring-utilization"></a>

To view resource utilization navigate to Analyze in the main navigation bar and click Utilization:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-17.png" alt="" height="640" width="826"><figcaption><p><strong>Figure 1 – Navigation to Cloud Utilization</strong></p></figcaption></figure>

This will open the utilization page and by default you will see three main sections:

1. **Search Bar**
2. **Resource types selector**
3. **List of resources**

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-18-1024x655.png" alt="" height="655" width="1024"><figcaption><p><strong>Figure 2 – Cloud Utilization Main Page</strong></p></figcaption></figure>

#### Searching <a href="#searching" id="searching"></a>

You can search by relevant resource properties and additionally, you can filter resources by recommendations (if applicable). For example, you can review all resources recommended for “shutdown” and see if utilization is low.

#### Resource Type Selector <a href="#resource-type-selector" id="resource-type-selector"></a>

Utilization currently support two resource types:

1. Virtual Machines (that includes Azure scale sets)
2. Storage accounts

Utilization supports both Azure and Amazon resource in one single unified view.

#### List of Resource <a href="#list-of-resource" id="list-of-resource"></a>

On the main page you will see a table with a list of your cloud resources with the main metric selected – for Virtual Machines it is _Average CPU_, and for Storage Accounts it is _Capacity_.

The table can be sorted by “all visible columns” so you can optimize your analysis.

### Resource Details <a href="#resource-details" id="resource-details"></a>

The core feature of utilization is plotting metrics. You can navigate to details by clicking “View” on the list.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-19-1024x667.png" alt="" height="667" width="1024"><figcaption><p><strong>Figure 3 – Resource Details</strong></p></figcaption></figure>

The page contains four main areas:

1. **Resource Basic Information**
2. **Date Range Selector**
3. **Metric Selector**
4. **Chart Area**

#### Resource Basic Information <a href="#resource-basic-information" id="resource-basic-information"></a>

This section contains information like group, subscription, provider and tags. Additionally you can navigate directly to [recommendation ](https://help.pyracloud.com/knowledge-base/recommendations/)or [resource ](https://help.pyracloud.com/knowledge-base/managing-tags-and-resources/)modules.

#### Date Selector <a href="#date-selector" id="date-selector"></a>

Currently there are two types of selectors – 30 days and 7 days (older data is automatically removed).

In “30 days” mode you see a daily aggregation chart (4) and in “7 days” chart you see hourly aggregation.

#### Metric Selector <a href="#metric-selector" id="metric-selector"></a>

This drop down allows you to view available metrics. The module currently support CPU and network traffic for Virtual Machines, and Capacity and Counters for storage accounts.

After selecting, the metric chart is adjusted automatically.

#### Chart Area <a href="#chart-area" id="chart-area"></a>

As well as plotting metrics data, the chart can also present scale set resources, so you can analyze multiple nodes running on scale set.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-21-1024x421.png" alt="" height="421" width="1024"><figcaption><p><strong>Figure 4 – Showing Scale Set Machine</strong></p></figcaption></figure>

By clicking on the legend (1) you can show / hide scale set nodes.

### Configuring Alerts <a href="#configuring-alerts" id="configuring-alerts"></a>

The utilization module supports custom alerts, so you can setup notifications based on the low utilization of your machines, or over utilization of your storage accounts.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-30-1024x187.png" alt="" height="187" width="1024"><figcaption><p><strong>Figure 5 – Creating Alerts</strong></p></figcaption></figure>

To create alerts, complete your search and then select the **Create Alert** button.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-31.png" alt="" height="426" width="344"><figcaption><p><strong>Figure 6 – Virtual Machine Alerts</strong></p></figcaption></figure>

By default, the alert modal appears with Virtual Machine (CPU) notifications. You can configure notifications to be alerted if machine utilization (from your search criterial) drops bellow (10%, 20% or a custom percentage).

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-33.png" alt="" height="387" width="374"><figcaption><p><strong>Figure 7 – Storage Alerts</strong></p></figcaption></figure>

You can also configure alerts based on capacity of the storage accounts. If it grows above a defined threshold you will then be notified.

**Note**: Alerts are generated once per day at 5AM UTC

### Configuring AWS Access <a href="#configuring-aws-access" id="configuring-aws-access"></a>

If the utilization module is not able to pull utilization metrics, you will see the below popup message:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-22-1024x222.png" alt="" height="222" width="1024"><figcaption><p><strong>Figure 8 – Unable to pull utilization metrics for AWS</strong></p></figcaption></figure>

Utilization uses CloudWatch to pull metrics. If you see the above message, it means CloudWatch was not assigned to **PyraCloudRole**.

To fix this, open the AWS Console and navigate to IAM.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-23.png" alt="" height="302" width="963"><figcaption><p><strong>Figure 9 – AWS – IAM</strong></p></figcaption></figure>

Then locate PyraCloudRole:

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-24-1024x812.png" alt="" height="812" width="1024"><figcaption><p><strong>Figure 10 – PyraCloud Role in IAM</strong></p></figcaption></figure>

In the role, open PyraCloud ReadOnlyPolicy.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-25-1024x156.png" alt="" height="156" width="1024"><figcaption><p><strong>Figure 11 – ReadOnlyPolicy</strong></p></figcaption></figure>

Then click **Edit policy**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-26.png" alt="" height="113" width="640"><figcaption><p><strong>Figure 11 – Edit PyraCloud Policy</strong></p></figcaption></figure>

Next, switch to JSON view.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-27-1024x505.png" alt="" height="505" width="1024"><figcaption><p><strong>Figure 12 – JSON View of PyraCloud Policy</strong></p></figcaption></figure>

In the editor please add “cloudwatch:GetMetricStatistics” and click Review on the bottom of the page.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-28-1024x463.png" alt="" height="463" width="1024"><figcaption><p><strong>Figure 13 – AWS JSON Role List</strong></p></figcaption></figure>

In the review summary you should see CloudWatch permission on the list.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/06/image-29-1024x409.png" alt="" height="409" width="1024"><figcaption><p><strong>Figure 14 – AWS Policy Review</strong></p></figcaption></figure>

If everything is ok, click **Save Changes**.

You have to repeat the above for all linked accounts if you are using AWS Organizations.

Utilization synchronizes data every hour, so on the next sync your utilization metrics should be synchronized with PyraCloud.
