# Role Assignment and GDAP Configuration

## Role assignment for GDAP requests

The following table outlines the roles that SoftwareOne may require to establish a granular admin relationship request. It also describes what each role enables.

**Service** - Microsoft Azure

| Role name                      | Description                                                                      |
| ------------------------------ | -------------------------------------------------------------------------------- |
| Directory reader​              | Can read basic directory information.                                            |
| Global reader                  | Can read everything that a Global Administrator can, but cannot update anything. |
| Service support administrator​ | Can read service health information and manage support tickets.                  |
| Billing administrator          | Performs common billing-related tasks, like updating payment information.        |

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

## Configuration

The GDAP admin relationship is established with the following configuration:

| Property           | Value                                        |
| ------------------ | -------------------------------------------- |
| displayName        | Microsoft Tenant Name + 'admin relationship' |
| duration           | P2Y                                          |
| autoExtendDuration | 180 days                                     |

Once the GDAP relationship is in place, its duration is set to 2 years by default. When the relationship is about to expire, it's automatically extended for an additional 180 days.&#x20;
