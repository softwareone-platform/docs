# What data do you collect for 365 Analytics?

### How does 365 Analytics connect to my data?

365 Analytics uses the Microsoft Graph service to access your customer tenant.&#x20;

This is managed through the use of an Enterprise Application provisioned in your Microsoft Entra directory and controlled through the use of security roles associated with the Enterprise Application. This enterprise application is called 'SoftwareOne Cloud Insider - Read Only' and is configured as part of the onboarding process.

### Encryption <a href="#encryption" id="encryption"></a>

365 Analytics makes extensive use of data encryption for data in transit and at rest:

* Traffic from 365 Analytics users is encrypted using HTTPS in their web browsers.
* API traffic between the 365 Analytics application and Microsoft’s services is all encrypted. Graph traffic is natively encrypted since it’s just HTTP requests; other protocols, such as remote PowerShell, are tunneled over HTTPS.
* All 365 Analytics data is encrypted at rest.
