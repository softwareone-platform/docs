# Reserved Instance Consumption Summary

Reservations help you save money by committing to a usage plan for multiple products (for example Virtual Machines and storage). Committing allows you to get a discount for resources you are using. RIs are one of the cost-saving strategies that can give you the biggest savings.

You can read more about other available cost optimization strategies in the [Cloud Cost Optimization](../../services/cloud-cost-optimization.md) topic.&#x20;

The usage plans depend on the cloud provider. For information on the usage plans, see the [Azure ](https://azure.microsoft.com/en-us/pricing/reserved-vm-instances/)and [AWS ](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html)websites.

***

### Gaining visibility into your reservations <a href="#gain-visibility-into-your-reservations" id="gain-visibility-into-your-reservations"></a>

With PyraCloud you can easily perform tasks related to managing cloud reservations, which allows you to accomplish the most savings.

PyraCloud gives you a central view to quickly check your reservation's health, and monitor savings, and utilization. This report is a part of our Spend Management Reporting feature and it is available here. We enable reporting automatically when our system detects an RI purchase.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/09/image-1024x364.png" alt=""><figcaption></figcaption></figure>

1. Recent average of your reservation utilization – you can check if there is any degradation in usage. If the average utilization is going down – resources that were utilizing RIs were likely deallocated.
2. PyraCloud keeps track of your historical purchases so you can compare values at any time. For monitoring purposes look at “Active” status only.
3. If you want to keep the reservation list for your internal records, you can export it to an XLS file.

#### Resources attached to RI <a href="#resources-attached-to-ri" id="resources-attached-to-ri"></a>

PyraCloud transforms billing data in a way that allows you to effortlessly explore resources utilizing your RI at a given point in time.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/reservation_details-1024x888.png" alt=""><figcaption></figcaption></figure>

1. Reservation details are exposed by the cloud provider.
2. The Amortized View groups data by resource, so you can see which resources are using this Reserved Instance. You can “drill down” to a selected month to see daily distribution.

You will notice **Reservation Unused Cost** in the chart legend, which informs you if the full potential of your RI is not realized.

\
You should keep this bar as low as possible (because of the delay in receiving data from cloud providers in the last 2 days you might see unused cost which is not accurate).

3. In the Utilization tab, you can monitor daily utilization of your reservation.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/reservation_utilization-1024x520.png" alt=""><figcaption><p>Reservation Daily utilization</p></figcaption></figure>

***

### Spend and Budget Management <a href="#spend-and-budget-management" id="spend-and-budget-management"></a>

PyraCloud creates resources for each reservation so that you can track costs in spend management, create budgets, or schedule a chargeback.

The lifetime of a resource is determined by the term, once expired resources will be marked as removed.

#### Predictions <a href="#predictions" id="predictions"></a>

We have incorporated RI metadata into our prediction engine. We assume that an RI will be renewed (if you don’t cancel it) so you may see “Purchase” spikes in your predictions, if enabled.

Additionally, monthly reservations will return predictions for every consecutive month.

***

### Alerting <a href="#alerting" id="alerting"></a>

We value your time, so we automatically created notifications for all your RI’s. As a result, we will send you an alert if the RI utilization drops below 80%.

If you want to receive an email or SMS, be sure to verify your subscription in the Consumption Section (1) of the Notification Hub.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/reservation_notification-1024x167.png" alt=""><figcaption><p>Notification rules configuration</p></figcaption></figure>

***

### Frequently Asked Questions <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

#### Why reservation utilization is not showing for my Azure Simple tenant <a href="#why-reservation-utilization-is-not-showing-for-my-azure-simple-tenant" id="why-reservation-utilization-is-not-showing-for-my-azure-simple-tenant"></a>

When a Microsoft tenant has conditional access policies enabled and is moved to a SoftwareOne partner account, PyraCloud automated onboarding may not be able to integrate correctly.

For PyraCloud to work, the customer must manually configure their tenant so that PyraCloud can access it. Follow these steps to onboard PyraCloud.

**Create the “PyraCloud (Azure)” Enterprise Application**

The first step is to perform consent. PyraCloud uses an Enterprise Application to access the customer tenant.

Important:

* You should launch this link in an InPrivate/Incognito/Private window to ensure you are signing in to the correct tenant.
* You must sign in with a user who has permission to perform consent.

To register for the Enterprise Application, use the following link: [Perform Consent](https://login.microsoftonline.com/common/oauth2/authorize?response\_type=code\&client\_id=2a4807a4-d9e4-457d-b32f-a455e0d3662a\&prompt=consent\&redirect\_uri=https://www.softwareone.com/)

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-11.png" alt="" height="575" width="437"><figcaption><p>Click accept after reviewing permissions</p></figcaption></figure>

**Confirm the Enterprise Application Exists**

To confirm the “PyraCloud (Azure)” Enterprise Application exists, sign in to the Azure portal and navigate to **Azure Active Directory** -> **Enterprise applications**.

The “PyraCloud (Azure)” application should be visible in the list. If it is not visible, try searching for “pyra”.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-12.png" alt=""><figcaption></figcaption></figure>

**Assign IAM Roles to the “PyraCloud (Azure)” Enterprise Application**

PyraCloud requires the following roles in each Azure subscription being activated:

* **Reader**: This role allows PyraCloud to import resources from your Azure subscription into PyraCloud. You can then manage these resources and tag them in the Tags and Resources features.
* **Tag Contributor**: This role is required to synchronize tags to and from your Azure subscription. PyraCloud will only synchronize tags back to your Azure subscription if you select write-back of tags in Cloud Tenant Setup. The default setting is read-only.

For assigning roles to subscriptions, see Grant Access to PyraCloud with Azure Management Groups.

Once completed, during the next scheduled synchronization, PyraCloud will be able to pull reservation utilization data.
