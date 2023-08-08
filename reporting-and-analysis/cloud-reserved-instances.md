# Cloud Reserved Instances

Reservations help you save money by committing to a usage plan for multiple products (for ex. Virtual Machines, Storage). Committing allows you to get a discount for resources you are using. RIs are one of the cost saving strategies that can give you the biggest saving.

You can read [more ](https://help.pyracloud.com/knowledge-base/cloud-cost-optimization/)about other available cost optimization strategies.

Usage plans depends on the cloud provider, to read more check out [Azure ](https://azure.microsoft.com/en-us/pricing/reserved-vm-instances/)or [AWS ](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html)websites.

### Gain visibility into your reservations <a href="#gain-visibility-into-your-reservations" id="gain-visibility-into-your-reservations"></a>

With PyraCloud you can easily perform tasks related to managing cloud reservations, which allows you to accomplish the most savings.

PyraCloud gives you a central view to quickly check your reservations health, monitor savings, and utilization. This report is a part of our [Spend Management Reporting](https://help.pyracloud.com/knowledge-base/cloud-consumption-overview/) feature and it is available [here](https://apps.pyracloud.com/report-designer/reports/f52a0728-054d-3048-b395-7c665866f9aa). We enable reporting automatically when our system detects an RI purchase.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2022/09/image-1024x364.png" alt="" height="364" width="1024"><figcaption><p>Reserved Instance summary overview</p></figcaption></figure>

1. Recent average of your reservation utilization – you can check if there are any degradation in usage. If the average utilization is going down – resource that were utilizing RIs were likely deallocated.
2. PyraCloud keeps track of your historical purchases so you can compare values at any time. For monitoring purposes look at “Active” status only.
3. If you want to keep the reservation list for your internal records, you can export it to a XLS file.

#### Resources attached to RI <a href="#resources-attached-to-ri" id="resources-attached-to-ri"></a>

PyraCloud transforms billing data in a way that allows you to effortlessly explore resources utilizing your RI at a given point in time.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/reservation_details-1024x888.png" alt="" height="888" width="1024"><figcaption></figcaption></figure>

1. Reservation details exposed by cloud provider
2. The Amortized View groups data by resource, so you can see which resources are using this Reserved Instance. You can “drill down” to a selected month to see daily distribution.

You will notice **Reservation Unused Cost** in the chart legend, which informs you if the full potential of your RI is not realized.\
You should keep this bar as low as possible (because of delay in receiving data from cloud provider in last 2 days you might see unused cost which is not accurate).

3. In Utilization tab you can monitor daily utilization of your reservation.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/reservation_utilization-1024x520.png" alt="" height="520" width="1024"><figcaption><p>Reservation Daily utilization</p></figcaption></figure>

### Spend and Budget Management <a href="#spend-and-budget-management" id="spend-and-budget-management"></a>

PyraCloud creates [resource ](https://help.pyracloud.com/knowledge-base/managing-tags-and-resources/)for each reservation so that you can track costs in[ spend management](https://help.pyracloud.com/knowledge-base/cloud-consumption-overview/), create [budgets](https://help.pyracloud.com/knowledge-base/creating-cloud-budgets/) or schedule a [chargeback](https://help.pyracloud.com/knowledge-base/creating-chargebacks/).

Lifetime of a resource is determined by the term, once expired resources will be marked as removed.

#### Predictions <a href="#predictions" id="predictions"></a>

We have incorporated RI metadata into our prediction engine. We assume that a RI will be renewed (if your don’t cancel it) so you may see “Purchase” spikes in in your predictions, if enabled.

Additionally, monthly reservations will return predictions for every consecutive month.

### Alerting <a href="#alerting" id="alerting"></a>

We value your time, so we automatically created [notifications](https://help.pyracloud.com/knowledge-base/cloud-consumption-alerts/) for all your RI’s. As a result, we will send you an alert if the RI utilization drops below 80%.

If you want to receive an email or SMS, be sure to verify your [subscription](https://apps.pyracloud.com/notifications/manage) in Consumption Section (1) of the Notification Hub.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/01/reservation_notification-1024x167.png" alt="" height="167" width="1024"><figcaption><p>Notification rules configuration</p></figcaption></figure>

### Frequently Asked Questions <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

#### Why reservation utilization is not showing for my Azure Simple tenant <a href="#why-reservation-utilization-is-not-showing-for-my-azure-simple-tenant" id="why-reservation-utilization-is-not-showing-for-my-azure-simple-tenant"></a>

When microsoft tenant has conditional access policies enabled and was moved to SoftwareOne partner account, PyraCloud automated onboarding may not be able to integrate correctly.

For PyraCloud to work, the customer must manually configure their tenant so that PyraCloud can access it. Follow these steps to onboard PyraCloud.

**Create the “PyraCloud (Azure)” Enterprise Application**

The first step is to perform consent. PyraCloud uses an Enterprise Application to access the customer tenant.

Important:

* You should launch this link in an InPrivate/Incognito/Private window to ensure you are signing in to the correct tenant.
* You must sign in with a user who has permission to perform consent.

To register the Enterprise Application, use the following link: [Perform Consent](https://login.microsoftonline.com/common/oauth2/authorize?response\_type=code\&client\_id=2a4807a4-d9e4-457d-b32f-a455e0d3662a\&prompt=consent\&redirect\_uri=https://www.softwareone.com/)

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-11.png" alt="" height="575" width="437"><figcaption><p>Click accept after reviewing permissions</p></figcaption></figure>

**Confirm the Enterprise Application Exists**

To confirm the “PyraCloud (Azure)” Enterprise Application exists, sign in to the Azure portal and navigate to **Azure Active Directory** -> **Enterprise applications**.

The “PyraCloud (Azure)” application should be visible in the list. If it is not visible, trying searching for “pyra”.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-12.png" alt="" height="438" width="748"><figcaption><p>The “PyraCloud (Azure)” Enterprise Application is visible in the list</p></figcaption></figure>

**Assign IAM Roles to the “PyraCloud (Azure)” Enterprise Application**

PyraCloud requires the following roles in each Azure subscription being activated:

* **Reader**: This role allows PyraCloud to import resources from your Azure subscription into PyraCloud. You can then manage these resources and tag them in the Tags and Resources features.
* **Tag Contributor**: This role is required to synchronize tags to and from your Azure subscription. PyraCloud will only synchronize tags back to your Azure subscription if you select write-back of tags in Cloud Tenant Setup. The default setting is read-only.

For assigning roles to subscription please refer to [Grant Access to PyraCloud with Azure Management Groups](https://help.pyracloud.com/knowledge-base/grant-access-to-pyracloud-with-azure-management-groups/)

Once completed, during next scheduled synchronization, PyraCloud will be able to pull reservation utilization data.

If you still having issues with reservation utilization kindly please reach out to PyraCloud support.
