# Reservation Monitoring - Cloud Reserved Instances

Reservations help you save money by committing to a usage plan for multiple products, such as virtual machines and storage.

Committing allows you to get a discount for resources you are using. RIs are one of the cost-saving strategies that can give you the biggest savings. You can read about the available cost optimization strategies in [Cloud Cost Optimization](../../../extensions/cloud-tools/cloud-cost-optimization.md). Note that the usage plans depend on the cloud provider. See the [Azure ](https://azure.microsoft.com/en-us/pricing/reserved-vm-instances/)and [AWS ](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-capacity-reservations.html)websites for information on the usage plans.

## Gaining visibility into your reservations <a href="#gain-visibility-into-your-reservations" id="gain-visibility-into-your-reservations"></a>

With the Marketplace Platform, you can manage cloud reservations for the most savings.

The platform gives you a central view to quickly check your reservation's health, and monitor savings, and utilization. This report is a part of our Spend Management Reporting. We enable reporting automatically when our system detects an RI purchase.

<figure><img src="../../../.gitbook/assets/image (705).png" alt=""><figcaption><p>Reserved Instance Consumption</p></figcaption></figure>

1. **Average utilization** - Indicates the recent average of your reservation utilization. You can check if there is any degradation in usage. If the average utilization is going down, resources that were utilizing RIs were likely deallocated.
2. **Status** - The Client Portal keeps track of your historical purchases so you can compare values at any time. For monitoring purposes, look at **Active** status only.
3. **Export** - If you want to keep the reservation list for your internal records, you can export it to an XLS file.

## Resources attached to RI <a href="#resources-attached-to-ri" id="resources-attached-to-ri"></a>

The Client Portal transforms billing data in a way that allows you to effortlessly explore resources utilizing your RI.

<figure><img src="../../../.gitbook/assets/image (706).png" alt=""><figcaption></figcaption></figure>

1. Reservation details are exposed by the cloud provider.
2. **Amortized View** - Groups data by resource, so you can see which resources are using this Reserved Instance. You can drill down to a selected month to see daily distribution.

{% hint style="info" %}
The **Reservation Unused Cost** in the chart legend indicates that the full potential of your RI is not realized. You should keep this bar as low as possible. Because of the delay in receiving data from cloud providers in the last 2 days, you might see unused costs, which is not accurate.
{% endhint %}

3. **Utilization** - Allows you to monitor the daily utilization of your reservation.

<figure><img src="../../../.gitbook/assets/image (707).png" alt=""><figcaption><p>Utilization tab</p></figcaption></figure>

## Spend and Budget Management <a href="#spend-and-budget-management" id="spend-and-budget-management"></a>

The Client Portal creates resources for each reservation so you can track costs in spend management, create budgets, or schedule a chargeback.

The lifetime of a resource is determined by the term. Once expired, the resources are marked as removed.

### Predictions <a href="#predictions" id="predictions"></a>

We have incorporated RI metadata into our prediction engine. We assume that an RI will be renewed (if you don’t cancel it) so you may see “Purchase” spikes in your predictions if enabled.

Additionally, monthly reservations will return predictions for every consecutive month.

### Alerting <a href="#alerting" id="alerting"></a>

We value your time, so we automatically created notifications for all your RIs. As a result, we will send you an alert if the RI utilization drops below 80%.

If you want to receive an email or SMS, be sure to verify your subscription in the Consumption Section (1) of the Notification Hub.

<figure><img src="../../../.gitbook/assets/image (710).png" alt=""><figcaption><p>Notification Hub</p></figcaption></figure>

## Frequently Asked Questions <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

### The reservation utilization isn't visible for my AzureSimple tenant <a href="#why-reservation-utilization-is-not-showing-for-my-azure-simple-tenant" id="why-reservation-utilization-is-not-showing-for-my-azure-simple-tenant"></a>

If a Microsoft tenant with conditional access policies is moved to a SoftwareOne partner account, the Client Portal automated onboarding might not work correctly.

In such cases, you must manually configure your tenant so that the Client Portal can access it. Follow these steps to configure the tenant:

1. **Create the “PyraCloud (Azure)” Enterprise Application** -  The first step is to perform consent. The Client Portal uses an Enterprise Application to access the tenant. To register for the Enterprise Application, use the following link: [Perform Consent](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code\&client_id=2a4807a4-d9e4-457d-b32f-a455e0d3662a\&prompt=consent\&redirect_uri=https://www.softwareone.com/)

{% hint style="info" %}
* Make sure to launch this link in an InPrivate/Incognito/Private window to ensure you are signing in to the correct tenant.
* You must sign in as a user who has permission to perform consent.
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (711).png" alt=""><figcaption><p>Microsoft sign in page</p></figcaption></figure>

2. **Confirm that the Enterprise Application exists** - To confirm the 'PyraCloud (Azure)' Enterprise Application exists, sign in to the Azure portal and navigate to **Azure Active Directory** > **Enterprise applications**. The **PyraCloud (Azure)** application should be visible in the list. If it's not visible, try searching for 'pyra'.

<figure><img src="../../../.gitbook/assets/image (712).png" alt=""><figcaption><p>PyraCloud (Azure) enterprise application</p></figcaption></figure>

3. **Assign the Reservation Reader role to the PyraCloud (Azure) Enterprise Application** - For information on how to assign the role, see [Assign the Reservations Reader role through Azure](../../../help-and-support/faqs/im-unable-to-view-the-reserved-instance-data.md#assign-the-owner-role-for-all-reservations-1).&#x20;
