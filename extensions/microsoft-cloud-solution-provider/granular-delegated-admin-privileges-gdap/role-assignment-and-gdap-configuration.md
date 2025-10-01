# Role Assignment and GDAP Configuration

### GDAP role assignment for CSP products purchased for self-use

When ordering CSP products for your own use through the Marketplace platform, SoftwareOne requires specific [granular delegated admin privileges (GDAP)](./) to effectively provision or manage these products in your Microsoft tenant.

The following table outlines the GDAP roles that SoftwareOne requires to establish a relationship. It also describes what each role enables.

**Service** - Microsoft Azure

<table><thead><tr><th width="361">Role name</th><th>Description</th></tr></thead><tbody><tr><td>Directory reader​</td><td>Can read basic directory information.</td></tr><tr><td>Global reader</td><td>Can read everything that a Global Administrator can, but cannot update anything.</td></tr><tr><td>Service support administrator​</td><td>Can read service health information and manage support tickets.</td></tr><tr><td>Billing administrator</td><td>Performs common billing-related tasks, like updating payment information.</td></tr></tbody></table>

**Service** - Microsoft 365 Business, Enterprise, & Apps (Charity, Commercial, and Education)

| Role name                        | Description                                                                                                                                                                                                                                                                                      |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Attack simulation administrator  | Can create and manage all aspects of attack simulation campaigns.                                                                                                                                                                                                                                |
| Authentication administrator​    | Can access to view, set and reset authentication method information for any non-admin user.                                                                                                                                                                                                      |
| Billing administrator            | Performs common billing-related tasks like updating payment information.                                                                                                                                                                                                                         |
| Compliance administrator         | Can read and manage compliance configuration and reports in Microsoft Entra ID and Microsoft 365.                                                                                                                                                                                                |
| Directory readers ​              | Can read basic directory information. Commonly used to grant directory read access to applications and guests.                                                                                                                                                                                   |
| Domain name administrator ​      | Manages domain names in cloud and on-premises.                                                                                                                                                                                                                                                   |
| Exchange administrator ​         | Manages all aspects of the Exchange product.                                                                                                                                                                                                                                                     |
| Global reader ​                  | Can read everything that a Global Administrator can, but not update anything.                                                                                                                                                                                                                    |
| Groups administrator ​           | Can create and manage groups, create and manage group settings like naming and expiration policies. Can also view group activity and audit reports.                                                                                                                                              |
| Hybrid identity administrator ​  | Manages Active Directory to Microsoft Entra cloud provisioning, Microsoft Entra Connect, pass-through authentication (PTA), password hash synchronization (PHS), seamless single sign-on (seamless SSO), and federation settings. Does not have access to manage Microsoft Entra Connect Health. |
| Intune administrator ​           | Manages all aspects of the Intune product.                                                                                                                                                                                                                                                       |
| License administrator            | Manages product licenses on users and groups.                                                                                                                                                                                                                                                    |
| Network administrator            | Manages network locations and reviews enterprise network design insights for Microsoft 365 Software as a Service applications.                                                                                                                                                                   |
| Fabric administrator (PowerBI) ​ | Manages all aspects of the Fabric and Power BI products.                                                                                                                                                                                                                                         |
| Power platform administrator     | Can create and manage all aspects of Microsoft Dynamics 365, Power Apps and Power Automate.                                                                                                                                                                                                      |
| Security administrator ​         | Can read security information and reports, and manage configuration in Microsoft Entra ID and Office 365.                                                                                                                                                                                        |
| Service support administrator ​  | Can read service health information and manage support tickets.                                                                                                                                                                                                                                  |
| SharePoint administrator ​       | Manages all aspects of the SharePoint service.                                                                                                                                                                                                                                                   |
| Skype for business administrator | Manages all aspects of the Skype for Business product.                                                                                                                                                                                                                                           |
| Teams administrator              | Manages the Microsoft Teams service.                                                                                                                                                                                                                                                             |
| User administrator               | Manages all aspects of users and groups, including resetting passwords for limited admins.                                                                                                                                                                                                       |
| Windows 365 administrator        | Can create and manage security groups but does not have administrator rights over Microsoft 365 groups.                                                                                                                                                                                          |
| Cloud application administrator  | Grants the ability to create and manage all aspects of enterprise applications and application registrations.                                                                                                                                                                                    |

**Service** - Microsoft Dynamics 365 (Charity, Commercial, and Education)

| Role name                        | Description                                                                                                                                            |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Authentication administrator​    | Can access to view, set and reset authentication method information for any non-admin user.                                                            |
| Billing administrator            | Performs common billing-related tasks like updating payment information.                                                                               |
| Directory readers ​              | Can read basic directory information. Commonly used to grant directory read access to applications and guests.                                         |
| Global reader                    | Can read everything that a Global Administrator can, but not update anything.                                                                          |
| Groups administrator ​           | Creates and manages groups and creates and manages group settings like naming and expiration policies. Can also view group activity and audit reports. |
| License administrator            | Manages product licenses on users and groups.                                                                                                          |
| Fabric administrator (PowerBI) ​ | Manages all aspects of the Fabric and Power BI products.                                                                                               |
| Power platform administrator​    | Can create and manage all aspects of Microsoft Dynamics 365, Power Apps and Power Automate.                                                            |
| Service support administrator ​  | Can read service health information and manage support tickets.                                                                                        |
| User administrator               | Manages all aspects of users and groups, including resetting passwords for limited admins.                                                             |
| Cloud application administrator  | Grants the ability to create and manage all aspects of enterprise applications and application registrations.                                          |

### GDAP role assignment for CSP products purchased for resale

If you are a SoftwareOne Partner purchasing [CSP products for resale](../../../marketplace-platform/getting-started/marketplace-for-partners/how-to-order-products-for-resale.md), your customers must approve a GDAP relationship request that includes the roles listed in the following table:

{% hint style="info" %}
These roles are not dependent on individual services, such as Azure or Dynamics, and apply to all CSP products purchased for resale.
{% endhint %}

<table><thead><tr><th width="284">Role</th><th>Description</th></tr></thead><tbody><tr><td>Global reader </td><td>Can read everything that a Global Administrator can, but cannot update anything.</td></tr><tr><td>Billing administrator </td><td>Can perform billing-related tasks, such as updating payment information.</td></tr><tr><td>Directory writers </td><td>Can read basic directory information. Commonly used to grant directory read access to applications and guests.</td></tr><tr><td>Cloud application administrator </td><td>Can create and manage all aspects of enterprise applications and application registrations.</td></tr><tr><td>License administrator </td><td>Manages product licenses for users and groups.</td></tr><tr><td>Service support administrator</td><td>Can read service health information and manage support tickets.</td></tr></tbody></table>

To learn more about GDAP and its importance, see [Granular Delegated Admin Privileges](./).

### GDAP configuration

The GDAP admin relationship is established with the following configuration:

| Property           | Value                                        |
| ------------------ | -------------------------------------------- |
| displayName        | Microsoft Tenant Name + 'admin relationship' |
| duration           | P2Y                                          |
| autoExtendDuration | 180 days                                     |

Once the GDAP relationship is in place, its duration is set to 2 years by default. When the relationship is about to expire, it's automatically extended for an additional 180 days.&#x20;
