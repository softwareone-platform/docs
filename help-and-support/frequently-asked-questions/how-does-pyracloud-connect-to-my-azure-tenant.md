# How does PyraCloud connect to my Azure tenant?

This article explains the importance of how PyraCloud connects to your Azure environment, how data is collected, and what security measures are in place.

***

### **Why does PyraCloud need an Access Token?**

An Access Token is used to enable PyraCloud to collect spend details about your Azure Subscriptions. Without this Access Token, we are unable to pull this detail and provide you with the analytics necessary to make decisions about your day-to-day spend.

***

### **What Admin Rights does SoftwareONE require for the PyraCloud Cloud Spend Management and/or Cloud Cost Optimization feature and service?**

The customer should be assigned the “Owner” role in the Azure subscriptions you wish to add to PyraCloud.

When adding Azure subscriptions, the SoftwareONE service principal is granted “Tag Contributor” access to those subscriptions. This level of access allows full access to the Azure subscription _without_ managing security settings. PyraCloud uses this access to retrieve a list of your resources (Virtual machines etc.) and the tags assigned to them. This role also provides a level of access to synchronize any user-assigned tags in PyraCloud back to the resources of the Azure subscription.  [Azure built-on roles reference](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-built-in-roles).

***

### **What is Tag Contributor**?

As per official Microsoft documentation: Tag Contributor 'lets you manage tags on entities, without providing access to the entities themselves' ([https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor](https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor)).

***

### **Why does PyraCloud require 'Tag Contributor' permissions?**

Being established as a 'Tag Contributor' allows PyraCloud to interact with customers' spend and resource data. Without this, we are unable to provide custom reporting, and consumption views and successfully implement other workstreams within PyraCloud Spend Management.

***

### **What happens when I perform consent?**

When you perform consent, you are redirected to Microsoft to accept permissions required by PyraCloud. As part of this process, PyraCloud is able to “impersonate” the consenting user for a short period (1 hour).

PyraCloud uses this impersonation to perform actions on behalf of the consenting user. This includes:

1. Assigning the Tag Contributor role to the PyraCloud application for subscriptions owned by the consenting user during onboarding. This is outlined in the Add your EA Microsoft Tenant and Subscriptions section of this document.
2. Assigning the Tag Contributor role to the PyraCloud application for subscriptions owned by the consenting user during the addition of more subscriptions to PyraCloud.&#x20;

***

### **What are the security implications of activating my tenant in PyraCloud?**

When the consent process is performed, a “service principal” is created in your tenant. This is conceptually similar to adding a user dedicated to PyraCloud for the purposes of accessing your tenant and subscriptions.

***

### **Do I have options to not synchronize resources or tags?**

Yes, PyraCloud offers application-level rights that you can change, after adding your Azure Subscriptions. Those include:

* No Resources - No resources or tags will be synchronized from subscriptions marked with this setting.
* No Tags – Your resources will be synchronized from your Azure Subscription, but their tags will not be synchronized in either direction.
* Read Tags Only - Your resources will be synchronized from your Azure Subscription, including their Tags. Any changes to Tags in PyraCloud will not be written back to Azure.
* Read and Write Tags (Default Role) – Your resources will be synchronized from your Azure Subscription, including their Tags. Any tag changes in PyraCloud will be written back to Azure.

Here is an example of how PyraCloud:

<figure><img src="../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure>

***

### **What can PyraCloud write back to my cloud provider?**

Only with Read/Write permissions enabled can PyraCloud write into a customer environment and write permissions are restricted to Tags only.

***

### **How do I secure PyraCloud from executing other functions within my cloud provider?**

RBAC in PyraCloud ensures that only a level of interaction that is acceptable to you is established between PyraCloud and your cloud provider.

***

### **Encryption**

PyraCloud makes extensive use of data encryption for data in transit:

* Traffic from the PyraCloud user is encrypted using HTTPS in their web browser
* API traffic between the PyraCloud platform and Microsoft’s services is all encrypted. Traffic is natively encrypted since it is an HTTPs request.

***

### **What is PAL and what data does it collect?**

Partner Admin Link (PAL) enables Microsoft to identify and recognize SoftwareONE as helping customers achieve business objectives and realized value in the cloud. Customers must first provide partner access to their Azure resource. Once access is granted, the SoftwareONE Microsoft Partner ID (MPN ID) is associated.

The PAL association to existing credentials provides no new customer data to Microsoft or SoftwareONE.

[Click here for source](https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/link-partner-id)
