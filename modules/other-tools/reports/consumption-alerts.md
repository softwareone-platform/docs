---
description: >-
  You can set up cloud consumption alerts so that you are notified when your
  cloud spend exceeds certain thresholds.
---

# Consumption Alerts

Consumption alerts are supported for IaaS/PaaS cloud platforms:

* Azure
* Amazon Web Services (AWS)

Currently, there are three types of cloud consumption alerts - **Spike Alerts**, **Overage Alerts,** and **Reserved Instance Utilization**.

* **Spike** **alerting** is designed to identify and alert you of usage anomalies in your Azure or AWS environments. You can configure usage thresholds, as well as communication preferences should your consumption exceed your defined threshold.

{% hint style="info" %}
By default, the Client Portal defines the alert threshold at a 25% spike in consumption compared to the previous month across all subscriptions.
{% endhint %}

You can also define consumption parameters over a period. The Overage Alert will notify you if the value is exceeded.

* **Overage alerting** gives very granular control, allowing you to set the consumption value as well as a period against which the service is monitoring consumption.
* **Reserved Instance alerting** allows you to set minimum utilization thresholds that monitor the consumption of your reservation purchase.

<figure><img src="../../../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure>

* The top section (1) describes Notification Hub settings. In the example above, you can see that this user only has Web notification enabled for both Spike and Overage alert types.
* The left Pane (2) is a list of all alerts for the past 30 days and the right pane (3) shows details about the currently selected alert.

### Accessing consumption alerts <a href="#post-1457-_toc14446607" id="post-1457-_toc14446607"></a>

You can access consumption alerts from any cloud consumption reports. You see the alert list by default. This report provides a basic overview of generated consumption alerts for every Cloud Provider that you configured.

### Consumption alerts section <a href="#consumption-alerts-section" id="consumption-alerts-section"></a>

Essentially two modules are available in consumption alerts:

* Consumption Alerts
* Manage Alert

#### Consumption alerts <a href="#post-1457-_toc19114679" id="post-1457-_toc19114679"></a>

This tab contains information about all generated alerts.

<figure><img src="../../../.gitbook/assets/image (680).png" alt=""><figcaption></figcaption></figure>

* The top section (1) describes Notification Hub settings. In the example above, you can see that this user only has Web notification enabled for both Spike and Overage alert types.
* The left Pane (2) is a list of all alerts for the past 30 days and the right pane (3) shows details about the currently selected alert.&#x20;

#### Managing alerts <a href="#post-1457-_toc19114680" id="post-1457-_toc19114680"></a>

This tab allows you to manage your alert definitions and notifications.

<figure><img src="../../../.gitbook/assets/image (681).png" alt=""><figcaption></figcaption></figure>

* **Create new alert** (1) opens a new interactive form where you can precisely configure your alert definition.
* **Manage Notification** (2), brings you to the Notification Hub configuration page, where you can precisely configure in which form you wish to see notifications.&#x20;
* In the **Alerts** section (3) you can see a list of all created alerts, along with the most important columns to quickly grasp the context of the definition.&#x20;
* **Subscribe** column (4) has a toggle button where you can subscribe/unsubscribe from particular definitions. If you are not subscribed, you will not receive any notification from that alert in any form.
* **Quick actions** (5) can be used to quickly modify or remove alert definitions.

### Understanding alert execution <a href="#post-1457-_understanding_alert_execution" id="post-1457-_understanding_alert_execution"></a>

The **Consumption Alerts** tab presents all created alerts. Alerts are evaluated once a day at 23:00 (Universal time zone)

#### New Execution Entries <a href="#post-1457-_toc19114682" id="post-1457-_toc19114682"></a>

New execution entries have a “New” badge and by default, you can view entries from the last 30 days. By clicking on an entry, you are marking it as read thus the “New” badge will be removed.

<figure><img src="../../../.gitbook/assets/image (682).png" alt=""><figcaption></figcaption></figure>

the To load more alerts, click “Load more” button when you reach the bottom of the execution list.

<figure><img src="../../../.gitbook/assets/image (683).png" alt=""><figcaption></figcaption></figure>

#### Execution details <a href="#post-1457-_toc19114683" id="post-1457-_toc19114683"></a>

The details section is loaded immediately after clicking on the alert from the left pane.

The top section (1) shows a brief explanation of why the alert was created, for example: _13.39 USD above the set threshold_.

<figure><img src="../../../.gitbook/assets/image (684).png" alt="" width="440"><figcaption></figcaption></figure>

You can also see details loaded directly from the alerts definition (2), like threshold, time range, and applied filters.&#x20;

The bottom section (3) shows the Filters that have been applied.

#### Alert preview <a href="#post-1457-_toc19114684" id="post-1457-_toc19114684"></a>

The preview section is a graphical representation of the alert and highlights the point of time when it occurs.

<figure><img src="../../../.gitbook/assets/image (685).png" alt=""><figcaption></figcaption></figure>

You can interact with this chart similarly to the Consumption Reports, which includes “hover-over text” when you are viewing a vertical bar in the chart.

#### Analyzing alerts in the consumption reports <a href="#post-1457-_toc19114685" id="post-1457-_toc19114685"></a>

The Alert item allows you to perform more detailed analysis in Consumption Reports so you can find the root cause of that alert. When you follow the “Analyze Consumption” link, the report will be opened in a new tab with the filters and dates extracted from the alert.

<figure><img src="../../../.gitbook/assets/image (686).png" alt=""><figcaption></figcaption></figure>

### Creating alert definition <a href="#post-1457-_creating_alert_definition" id="post-1457-_creating_alert_definition"></a>

#### Notification hub settings <a href="#post-1457-_notification_hub_settings" id="post-1457-_notification_hub_settings"></a>

Notification configuration allows you to set your preferred delivery methods for the alerts you have configured. The configuration page can be accessed by clicking on the “Notification Hub” link or “bell” icon in the top menu bar.

Once the Notification Hub page appears, a section for consumption settings is displayed. This is where you can individually configure delivery methods for Spike and Overage alert types.

<figure><img src="../../../.gitbook/assets/image (687).png" alt=""><figcaption></figcaption></figure>

#### Adding alert definition <a href="#post-1457-_alert_parameters" id="post-1457-_alert_parameters"></a>

You can access the wizard by clicking **Create New Alert** or **Edit**. Remember that the alert name has to be unique across all of your alerts.

<figure><img src="../../../.gitbook/assets/image (688).png" alt=""><figcaption></figcaption></figure>

#### Alert types <a href="#post-1457-_toc19114689" id="post-1457-_toc19114689"></a>

Notification alerting supports the following two modes:

* **Spike mode** is used to detect anomalies in your consumption characteristics, for instance, a Virtual Machine that was left running after performance tests executed by the team.
* **Overage mode** is used to track if the overall consumption is in the defined boundary (threshold).

<figure><img src="../../../.gitbook/assets/image (689).png" alt=""><figcaption></figcaption></figure>

#### Parameters <a href="#post-1457-_spike_alert_type" id="post-1457-_spike_alert_type"></a>

Parameters allow you to control the behavior and data scope of the alert. By choosing **All Tenants** or **All Subscriptions** each tenant or subscription will be monitored separately.

For example, you configured the threshold as follows:

* 14 days, and
* Spend increase of 25%

This means that the above rule will be applied individually to all subscriptions or tenants. If the condition is met, a notification will be produced.

<figure><img src="../../../.gitbook/assets/image (690).png" alt=""><figcaption></figcaption></figure>

The Custom option works slightly differently. First, you need to select a report type (1) and then you can precisely craft your definition, using that report (2).&#x20;

For instance, you may only want to monitor virtual machines in a single subscription. To do that in the report selector (1) you should select **Azure EA Consumption Details**, then select **Virtual Machine** in the Meter Category, and then narrow down the subscription filter according to your requirements.

<figure><img src="../../../.gitbook/assets/image (691).png" alt=""><figcaption></figcaption></figure>

If you are actively using the **Save Filters** functionality, you can click **Save Search** and all saved filter combinations will be available.

#### Threshold Configuration <a href="#post-1457-_toc19114691" id="post-1457-_toc19114691"></a>

In this section, you are configuring the criteria of the alert. First, you select the time context in which the average or sum cost will be calculated from (1). Then you should decide on the % or cost threshold to monitor (2).

For example, on a Spike Alert, by selecting 14 days, the average from the last two weeks will be calculated. Let’s assume the result is **100 USD**. You now set your threshold to **25%**. Your consumption will be monitored and any spend that is greater than **125 USD** will be reported as notification.

Additionally, you can control two extra parameters (3):

* **Ignore days with no spend**:  If enabled, it means that days with no consumption will not be counted within the average. For example, disabling Virtual Machines during the weekends.
* **Minimum alert value**: This means that you will be notified only when criteria (1) are met and the spending is greater than the provided value. This is helpful when monitoring spend under a specific value and a spike in these scenarios may be too noisy. For example, you may have a daily spend of $5, so a spike to $10 may not be as relevant until that spike exceeds a certain amount (like $100).

#### Visibility Configuration <a href="#post-1457-_toc19114692" id="post-1457-_toc19114692"></a>

Alert definitions can be private. A private alert means that it will only be visible to you (1). A public alert means that you can share this alert configuration with anyone in your company (2).

<figure><img src="../../../.gitbook/assets/image (692).png" alt=""><figcaption></figcaption></figure>

When you select **share with your team**, an additional dropdown appears where you can add team members individually. By default people with whom the alert is shared are unsubscribed – they have to subscribe to the alert to see notifications, this prevents you from generating unwanted notifications on other user’s accounts.

<figure><img src="../../../.gitbook/assets/image (693).png" alt=""><figcaption></figcaption></figure>
