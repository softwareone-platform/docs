# How does the platform connect to my Azure tenant?

This article explains how the platform connects to your Azure environment, how data is collected, and what security measures are in place.

### Why does the platform need an Access Token?

An Access Token is used to enable the platform to collect spend details about your Azure Subscriptions. Without this Access Token, we are unable to pull this detail and provide you with the analytics necessary to make decisions about your day-to-day spending.

### What admin rights does SoftwareOne require for Cloud Spend Management and Cloud Cost Optimization?

The customer must be assigned the “Owner” role in the Azure subscriptions you wish to add to the Client Portal.

When adding Azure subscriptions, the SoftwareOne service principal is granted “Tag Contributor” access to those subscriptions. This level of access allows full access to the Azure subscription _without_ managing security settings.&#x20;

The Client Portal uses this access to retrieve a list of your resources (Virtual machines, etc.) and the tags assigned to them. This role also provides a level of access to synchronize any user-assigned tags in the Client Portal back to the resources of the Azure subscription.  [Azure built-on roles reference](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-built-in-roles).

### What is Tag Contributor?

Tag Contributor lets you manage tags on entities, without providing access to the entities themselves. For more information, see the [Microsoft documentation](https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor).

### Why does the platform require 'Tag Contributor' permissions?

Being established as a 'Tag Contributor' allows the platform to interact with customers' spending and resource data. Without this, we are unable to provide custom reporting and consumption views and successfully implement other workstreams within Spend Management.

### What happens when I perform consent?

When you perform consent, you are redirected to Microsoft to accept permissions required by the platform. As part of this process, the platform can “impersonate” the consenting user for a short period (1 hour).

The platform uses this impersonation to perform actions on behalf of the consenting user. This includes:

1. Assigning the Tag Contributor role to the platform for subscriptions owned by the consenting user during onboarding.&#x20;
2. Assigning the Tag Contributor role to the platform for subscriptions owned by the consenting user during the addition of more subscriptions to the platform.

### What are the security implications of activating my tenant?

When the consent process is performed, a 'service principal' is created in your tenant. This is conceptually similar to adding a user dedicated to the Client Portal for the purposes of accessing your tenant and subscriptions.

### Do I have options to not synchronize resources or tags?

Yes, the platform offers application-level rights that you can change after adding your Azure Subscriptions. Those include:

* No Resources - No resources or tags will be synchronized from subscriptions marked with this setting.
* No Tags – Your resources will be synchronized from your Azure Subscription, but their tags will not be synchronized in either direction.
* Read Tags Only - Your resources will be synchronized from your Azure Subscription, including their Tags. Any changes to Tags in the platform will not be written back to Azure.
* Read and Write Tags (Default Role) – Your resources will be synchronized from your Azure Subscription, including their Tags. Any tag changes in the platform will be written back to Azure.

### What can the platform write back to my cloud provider?

When the Read/Write permissions are enabled, the platform can write into a customer environment. Write permissions are restricted to Tags only.

### How do I secure the platform from executing other functions within my cloud provider?

Role-based access control (RBAC) in the platform ensures that only a level of interaction that is acceptable to you is established between the platform and your cloud provider.

Encryption

The platform makes extensive use of data encryption for data in transit:

* Traffic from the platform is encrypted using HTTPS in their web browser.
* API traffic between the platform and Microsoft’s services is all encrypted. Traffic is natively encrypted since it is an HTTPS request.

### What is PAL, and what data does it collect?

Partner Admin Link (PAL) enables Microsoft to identify and recognize SoftwareOne as helping customers achieve business objectives and realize value in the cloud. Customers must first provide partner access to their Azure resources. Once access is granted, the SoftwareOne Microsoft Partner ID (MPN ID) is associated.

The PAL association with existing credentials provides no new customer data to Microsoft or SoftwareOne. For more information, see the [Microsoft documentation](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/link-partner-id).&#x20;
