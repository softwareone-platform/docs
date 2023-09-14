---
description: Understand what data 365 Analytics collects and why.
---

# What data do you collect for 365 Analytics?

***

### **What are service accounts and what do they do?** <a href="#service-accounts-and-what-they-do" id="service-accounts-and-what-they-do"></a>

Microsoft offers two primary API sets for accessing M365 services called PowerShell and Microsoft Graph.&#x20;

* PowerShell access requires the 365 Analytics application to authenticate to the service using a named credential instead of the enterprise application registration. That’s where the service accounts come in. 365 Analytics supports Reporting Service Accounts.
* Graph API access is managed through the Azure AD enterprise applications deployed as part of 365 Analytics provisioning in a tenant.

***

### **Reporting Service Accounts** <a href="#reporting-service-accounts" id="reporting-service-accounts"></a>

The Reporting Service Account is used to gather data from the target tenant using both PowerShell and Microsoft Graph. It is a read-only account and is required for all tenants. We recommend and have tested assigning the Global Administrator role to this account.

To learn about creating service accounts for 365 Analytics reporting, see [How to create service accounts for 365 Analytics reporting](how-to-create-service-accounts-for-365-analytics-reporting.md).

***

### **Encryption** <a href="#encryption" id="encryption"></a>

365 Analytics makes extensive use of data encryption for data in transit and at rest:

* Traffic from 365 Analytics users is encrypted using HTTPS in their web browser.
* API traffic between the 365 Analytics application and Microsoft’s services is all encrypted. Graph traffic is natively encrypted since it’s just HTTP requests; other protocols, such as remote PowerShell, are tunneled over HTTPS.
* All 365 Analytics data is encrypted at rest.

***

### **Service account credential storage** <a href="#service-account-credential-storage" id="service-account-credential-storage"></a>

All service account credentials held by 365 Analytics for reporting are stored and encrypted in two places:

* The Service Account password is encrypted before it leaves the client machine setting the password; whether that is via the User Interface or PowerShell script. It is therefore sent in an encrypted form to our backend servers. Only our job collection servers have the private key to decrypt this password.
* The encrypted service account password is then further protected by being stored in Azure Key Vaults, where only our ‘job engines’ (those services that collect data) have access to the key vault to obtain the data.

***

### **Multi-factor authentication and conditional access** <a href="#multi-factor-authentication-and-conditional-access" id="multi-factor-authentication-and-conditional-access"></a>

As of May 2020, Microsoft does not support the use of multi-factor authentication (MFA) for accounts used as service accounts in Office 365. This is **not** a 365 Analytics limitation, it’s a restriction imposed by Microsoft.&#x20;

The default policies applied by the service will break 365 Analytics service account access because they require MFA for accounts that hold the Global administrator role.

Microsoft’s recommended solution is to enable conditional access whitelisting for the IP addresses used to access M365 services using these service accounts.

{% hint style="info" %}
**NOTE:** The default conditional access policies available to all Office 365 customers do not support whitelisting; customers who do not currently have O365 licenses with support for the full set of conditional access features may need to purchase additional licenses from Microsoft.
{% endhint %}

If you require a list of IP addresses used for the reporting service account, contact [marketplace-support@softwareone.com](mailto:marketplace-support@softwareone.com).
