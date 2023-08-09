---
description: >-
  You can optimize, improve, and secure your software and cloud environment with
  intelligent recommendations.
---

# Working with Recommendations

The Recommendations module is a set of functionalities that facilitate intelligent recommendations and suggestions to optimize, streamline, and improve your software environment, be that on-premise or the cloud.

The Recommendations module offers recommendations from a variety of sources, such as Azure Advisor, AWS Cost Explorer, and AWS Trusted Advisor as well as integrating with SoftwareONE Services to provide bespoke and tailored recommendations that optimize a customer’s software environment.

Additionally, the Recommendation module provides capabilities to track metrics such as realized savings and completed recommendations for example, so these can be further used to track, manage, and report on savings opportunities and other key success metrics as well as justify return on investment.

***

### Accessing Recommendations <a href="#how-to-access-recommendations" id="how-to-access-recommendations"></a>

You can access the Recommendations module from the main navigation menu as well as the Software Asset Management and Cloud dashboard templates.

**To access Recommendations from the main menu**

* Navigate to **Analyze** and select **Recommendations**.

**To access Recommendations through the dashboard**

1. Open the Software Asset Management or Cloud dashboard template.
2. Select the SLM Recommendations or Azure Recommendations tile depending on the template that you open.
   * The tiles on these dashboards will navigate you to the appropriate section within the Recommendations module. For example, selecting the SLM Recommendations tile in the Software Asset Management Dashboard will navigate you to the Software Lifecycle Management Saving Recommendations.
   * In the Cloud Dashboard, selecting the Azure Recommendations tile will navigate you to the Azure Saving Recommendations, and clicking on the AWS Recommendations tile will navigate you to the AWS Saving Recommendations within the Recommendations module.

***

### Overview Page <a href="#overview-page" id="overview-page"></a>

The Recommendations module comes equipped with multiple views to help you understand and visualize recommendations in various ways. The Overview page is an analytics-based view that helps you understand how recommendations are associated with various parts of your infrastructure and how they are tracked i.e. potential or completed.

All customer recommendations are divided into three areas:

* Cost Optimization
* Operational Excellence
* Security

Tiles on the Overview page enable you to understand how recommendations are distributed across different areas, and how advanced you are in implementing them. Additionally, below each tile, you can find information about the most impactful recommendation type.

<figure><img src="../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

As mentioned previously, the Recommendation module presents data from different sources. This information is presented in the grid below the tiles. This view helps you to understand where your biggest opportunities to improve are.

<figure><img src="../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

#### **Cost Optimization** <a href="#cost-optimization" id="cost-optimization"></a>

The Cost Optimization page enables you to understand the potential savings structure. On the grid, you can find information about realized and active saving recommendations.

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

At the top of the page, there are filters that allow you to filter recommendations. All charts are adjusted for the provided search criteria.

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

You can find more details for each recommendation type by clicking on it. This will open up more information about Potential and Realized saving.

<figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

#### **Operational Excellence** <a href="#operational-excellence" id="operational-excellence"></a>

The Operational Excellence page enables you to understand the Operational Excellence recommendations structure. On the grid, you can find information about realized and active Operational Excellence recommendations. At the top of the page, there are filters that allow you to filter recommendations. All charts are adjusted for the provided search criteria.

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

You can find more details for the Operational Excellence recommendation type by clicking on it.

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

#### **Security** <a href="#security" id="security"></a>

The Security page enables you to understand the Security recommendations structure. On the grid, you can find information about realized and active Security recommendations. At the top of the page, there are filters that allow users to filter recommendations. All charts are adjusted for the provided search criteria.

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

You can find more details about the Security recommendation type by clicking on it.

<figure><img src="../../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

***

### Recommendation Features <a href="#recommendation-features" id="recommendation-features"></a>

The Recommendations module provides recommendations for on-premise and cloud environments. All recommendations come with a set of capabilities offered as part of the Recommendations platform. Some of these are:

* Ability to collaborate with your peers and SoftwareONE services through messaging and mentions.
* Ability to track the progress of every recommendation along with notes at every stage of the recommendation.

Let us look at these features in more detail below.

#### Messaging <a href="#messaging" id="messaging"></a>

You can collaborate on recommendations by using the messaging features. Simply click on a Recommendation from the grid and then navigate to the Messages tab.

The messaging feature allows stakeholders to participate in a conversation, so multiple collaborators can keep on top of recommendations and their progress. Through the use of the ‘mentions’ feature, users can tag their peers or SoftwareONE Services Consultants to bring items, to-do lists or issues to their attention.

This is available by typing ‘@’ and then typing the user’s first/last name, and selecting their name from the dropdown. When a user is mentioned in a conversation, an email is sent to the mentioned user as a notification. These email notifications cannot be turned off.

#### Progress Log <a href="#progress-log" id="progress-log"></a>

Every recommendation can be tracked through its lifecycle with the progress log functionality. You can track progress by navigating to the progress log.

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

#### Marking a Recommendation as Complete <a href="#marking-a-recommendation-as-complete" id="marking-a-recommendation-as-complete"></a>

All recommendations can be marked as complete from the Recommendation Type page when completed. There is an option to complete one or all recommendations of the given type.

For Azure and AWS recommendations, you don’t need to Mark recommendations as Complete because the Recommendations system automatically detects when recommendations are being executed and moves them to the completed/realized state. However, there are some exceptions to automatically realizing savings amounts from Azure and AWS Recommendations. For details, see [Completion of Azure Recommendations](working-with-recommendations.md#completion-of-azure-recommendations) and [AWS Recommendations](working-with-recommendations.md#aws-recommendations).

<figure><img src="../../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

Once a recommendation has been completed, it is moved from the Active tab on the main page to the Realised tab.

#### Dismissing a Recommendation <a href="#dismissing-a-recommendation" id="dismissing-a-recommendation"></a>

If a recommendation is not planned to be actioned on, you can dismiss the recommendation from the Recommendation type page. There is an option to dismiss all recommendations of the given type.

<figure><img src="../../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

### SLM Recommendations <a href="#slm-recommendations" id="slm-recommendations"></a>

Software Lifecycle Management (SLM) Recommendations are recommendations that are categorized into the following categories:

* **Savings:** These recommendations when actioned can enable cost savings.
* **Risk:** These recommendations help mitigate compliance risk for licenses that seem to come from a non-compliance position.

### Azure Recommendations <a href="#azure-recommendations" id="azure-recommendations"></a>

Azure Recommendations are recommendations that are categorized under the following Categories:

* **Savings** – These recommendations when actioned can enable cost savings.
* **Risk** – These recommendations help mitigate compliance risk for licenses that seem to come from a non-compliance position.
* **Security** – These recommendations help to improve the security of the Azure environment.
* **High Availability** – These recommendations help to improve the high availability of the Azure environment.
* **Performance** – These recommendations help improve the performance of the Azure environment

All Azure Recommendations have a Cloud Recommendation Type. For recommendations recommended by Azure, some examples of recommendation types are:

* Buy Reserved Instances
* Shutdown or Resize your Virtual Machine
* Security Center Recommendations
* Enable Soft Delete
* Enable Backup etc.

#### Associating Recommendations with Resources <a href="#associating-recommendations-with-resources" id="associating-recommendations-with-resources"></a>

All Azure recommendations that have been recommended by ‘Azure’ (and not by SoftwareONE services), are automatically associated with resources whether they are virtual machines, storage accounts, databases, etc.

For example, Recommendations of type ‘SQL DB Advisor recommendations’ are associated with SQL databases that need to be acted on.

The association from a recommendation to a related PyraCloud resource is available in the Related Resources tab on the Recommendation Details page.

<figure><img src="../../.gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>

#### Completion of Azure Recommendations <a href="#completion-of-azure-recommendations" id="completion-of-azure-recommendations"></a>

PyraCloud can detect the completion of Recommendations in Microsoft Azure. When a recommendation is detected as being completed on Azure, the status on that recommendation will automatically be set to Completed, and the potential savings amount on the recommendations will be set to Realised. When this happens, the recommendation will be moved from the Active tab to the Realised tab, and the realized savings from the recommendation will start to reflect on the Savings tile on the Azure tab.

{% hint style="info" %}
**NOTE**: PyraCloud does not track the realization of Reserved Instance recommendations from Microsoft Azure. This means when recommendations of the type ‘Buy Reserved Instances’ or ‘Renew Reserved Instances’ are completed i.e. PyraCloud will not track any savings realized as part of completing these recommendations.
{% endhint %}

### AWS Recommendations <a href="#aws-recommendations" id="aws-recommendations"></a>

PyraCloud downloads Recommendations for AWS from AWS Trusted Advisor and AWS Cost Explorer.

The AWS tab displays six tiles at the top. These are:

* **Savings:** These recommendations, when actioned, can enable cost savings.
* **Security:** These recommendations help to improve the security of the Azure environment
* **High Availability:** These recommendations help to improve high availability of the Azure environment
* **Performance:** These recommendations help improve the performance of the Azure environment

#### AWS Trusted Advisor <a href="#aws-trusted-advisor" id="aws-trusted-advisor"></a>

[AWS Trusted Advisor](https://aws.amazon.com/premiumsupport/technology/trusted-advisor/) is a source for recommendation data within AWS, that is available for any environment that is configured with the correct AWS Support Plan i.e. Business or Enterprise. AWS Trusted Advisor provides information for various recommendation categories, for example, Savings, Security, Performance, High Availability, Service Limits, etc.

Recommendations can be fetched from the AWS Trusted Advisor if:

* AWS Business or Enterprise [support plan](https://aws.amazon.com/premiumsupport/plans/) is enabled for an account within AWS.&#x20;
* The right permissions are enabled for AWS account(s) within PyraCloud. For information on permission required to download recommendations from AWS Trusted Advisor, see [Reonboarding AWS Recommendations](../../set-up/cloud-tenant-setup/aws-onboarding/updating-your-aws-account-permissions.md#re-onboard-aws-recommendations).

#### AWS Cost Explorer <a href="#aws-cost-explorer" id="aws-cost-explorer"></a>

[AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) is a source for recommendation data within AWS, that is available to any environment that has Cost Explorer turned on within AWS. PyraCloud is able to fetch Reservation-based recommendations from the Cost Explorer if Cost Explorer is enabled within AWS. These reservation-based recommendations are Reserved Instance (RI) purchase recommendations that could help you reduce your costs.

Recommendations can be fetched from the AWS Cost Explorer if:

* [Cost Explorer is enabled within AWS](https://docs.aws.amazon.com/cost-management/latest/userguide/ce-enable.html).
* Cost Explorer is enabled for your AWS Account within Cloud Tenant Setup in PyraCloud. This is enabled by default.

By default, all your AWS accounts will be configured to pull recommendations from AWS Cost Explorer.

**Synchronization Schedule:** The synchronization with AWS Cost Explorer happens once a week (as opposed to all recommendations-related synchronization processes that run once an hour), and this schedule is not configurable at the moment. This is so we are able to minimize costs, as fetching data from Cost Explorer is chargeable.

Charges for synchronizing AWS Cost Explorer RecommendationsPlease be aware that AWS charges 0.05 USD per account for every sync. PyraCloud will sync recommendation data per account once a week. When Cost Explorer is turned on (within AWS and PyraCloud), this should be a maximum of 0.20 USD per AWS account per month.

To turn off these recommendations, see [How to turn off Cost Explorer Recommendations](../../help-and-support/frequently-asked-questions/how-to-turn-off-the-cost-explorer-recommendations.md).

To effectively utilize these recommendations, make sure AWS Cost Explorer is turned on within AWS for each of your accounts. See [Enabling Cost Explorer](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/ce-enable.html) to turn on Cost Explorer within AWS.

### Office 365 Recommendations <a href="#office-365-recommendations" id="office-365-recommendations"></a>

Office 365 recommendations are recommendations from SoftwareOne that you can take advantage of. These recommendations will be populated by your SoftwareOne Services Account team, so you can make the best use of your Office 365 environment.

#### Recommendation Types for Office 365 Recommendations <a href="#recommendation-types-for-office-365-recommendations" id="recommendation-types-for-office-365-recommendations"></a>

All Office 365 Recommendations have a Cloud Recommendation Type. Some examples of recommendation types are:

* License Cleanup & Reconciliation (Category – Savings)
* Shared Mailbox Size – Mailbox approaching 50GB (Category – Savings)
* SecureScore Recommendation – Device (Category – Security)
* SecureScore Recommendation – Apps (Category – Security)
* SecureScore Recommendation – Identity (Category – Security)
* SecureScore Recommendation – Data (Category – Security)
* Email Forwarding (Category – Security)
* Empty Groups (Category – Infrastructure Hygiene)
* Inactive Distribution Groups (Category – Infrastructure Hygiene)
* Inactive Mail Recipients (Category – Infrastructure Hygiene)
* Email Archive (Category – Infrastructure Hygiene)

#### Advanced Filters for Office 365 Recommendations <a href="#advanced-filters-for-office-365-recommendations" id="advanced-filters-for-office-365-recommendations"></a>

Office 365 Recommendations can be filtered by a set of advanced criteria:

| Category                  | Possible options are **Savings**, **Security**, Infrastructure Hygiene, New Features/Updates, and **Others**.                                                                                                                                                                  |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Provider                  | Possible options are **Software Asset Management**, **Azure**, **AWS**, and **Office 365**.                                                                                                                                                                                    |
| Cloud Recommendation Type | These are alert statuses associated with the Recommendation such as **Unread**, **Updated**, and **Expires soon**.                                                                                                                                                             |
| Severity                  | Possible options are **High**, **Medium**, and **Low Impact**.                                                                                                                                                                                                                 |
| Alert                     | These are alert statuses associated with the Recommendation such as **Unread**, **Updated**, and **Expires soon**.                                                                                                                                                             |
| Owner                     | This is the name of the person to whom the recommendation can be assigned. Recommendations can be assigned to a member of the SoftwareOne Consultant team working with the customer, or any user within the customer for better tracking and management of the recommendation. |
