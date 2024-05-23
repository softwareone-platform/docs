# How does the platform access my Microsoft 365 tenant under CSP?

The platform imports information from your Microsoft 365 tenant daily. The data is used in the following features:

1. **Tag & Resource Manager** - Used to allocate resource costs to business units (custom groups), Tag & Resource Manager (TRM) imports information about Azure AD user accounts including (but not limited to) usernames, display names, departments, managers, addresses, and extensionAttributes. This information is used to help the user allocate license costs to the correct business unit. TRM also imports information about specific Microsoft 365 licenses assigned to users.
2. **Consumption** - Used to report on resource usage and cost, Consumption imports information about overall Microsoft 365 license quantities and assignments. This includes total purchased licenses, total assigned licenses, and total unassigned licenses for each subscription.

The Marketplace platform does not access a customer's tenant on an ad-hoc basis for any reason related to Microsoft 365.

## Authentication <a href="#authentication" id="authentication"></a>

The platform uses an account called `mfa.setup` to access the Partner Center API for CSP customers. In some instances, the platform also 'double hops' into a customer's Microsoft tenant to get information about users and license assignments.

This account is used to access the Microsoft Graph API, specifically, the users and SubscribedSkus endpoints that provide the Client Portal with information about Azure AD users. It also provides information such as, how many licenses from each Microsoft 365 subscription are assigned and how many are free. To learn more about these APIs, see the Microsoft documentation on [List users](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0\&tabs=http) and [List subscribedSkus](https://learn.microsoft.com/en-us/graph/api/subscribedsku-list?view=graph-rest-1.0\&tabs=http).

To authenticate and consume these APIs, the platform uses app+user authentication. It means that when the platform  authenticates, it uses a combination of both an Enterprise Application and a User Account (which is a service account, the aforementioned `mfa.setup` user).

For CSP, both these principles exist in SoftwareOne's Azure AD rather than in the customer's Microsoft tenant. For more information, see the Microsoft documentation on [App+User Authentication](https://learn.microsoft.com/en-us/partner-center/developer/partner-center-authentication#app--user-authentication).

Note that even under the new secure application model, app+user authentication is still used.

## Conditional Access policies

Unless configured, the Conditional Access policies (CAP) don't block authentication attempts by the enterprise applications. On the other hand, user account access can be actively blocked by CAP unless an exception is configured.

Historically, it has been challenging to configure exceptions for the user accounts in partner (SoftwareOne's) Microsoft tenants because they don't exist in the customer's Microsoft tenant.

Recently, Microsoft has added functionality to CAP to allow narrow (least privilege) exceptions to be configured for partner Microsoft tenants. For information, see [How to Configure Conditional Access Policies](how-to-configure-conditional-access-policies.md) and [Conditional Access for External Users (Microsoft documentation)](https://learn.microsoft.com/en-us/azure/active-directory/external-identities/authentication-conditional-access#conditional-access-for-external-users).

## Imported data fields

The following fields are downloaded for each user in the customer's Azure AD and Microsoft 365 subscriptions.

{% hint style="info" %}
&#x20;These fields are not customizable in the platform. They must all be downloaded.
{% endhint %}

| Azure AD users                | Microsoft 365 subscriptions                                                                                          |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| DisplayName                   | SkuId                                                                                                                |
| CompanyName                   | SkuPartNumber                                                                                                        |
| Department                    | SkuPrepaidUnits (Total purchased licenses)                                                                           |
| Mail                          | SkuConsumedUnits (Total assigned licenses)                                                                           |
| GivenName                     | SkuServicePlans (Products associated with the subscription, for example, Office 365 includes Teams and Yammer, etc.) |
| Surname                       | ﻿                                                                                                                    |
| JobTitle                      | ﻿                                                                                                                    |
| State                         | ﻿                                                                                                                    |
| PostalCode                    | ﻿                                                                                                                    |
| StreetAddress                 | ﻿                                                                                                                    |
| City                          | ﻿                                                                                                                    |
| PreferredLanguage             | ﻿                                                                                                                    |
| UsageLocation                 | ﻿                                                                                                                    |
| AssignedLicenses              | ﻿                                                                                                                    |
| UserPrincipalName             | ﻿                                                                                                                    |
| OfficeLocation                | ﻿                                                                                                                    |
| OnPremisesExtensionAttributes | ﻿                                                                                                                    |
| Country                       | ﻿                                                                                                                    |
| State                         | ﻿                                                                                                                    |
| UserType                      | ﻿                                                                                                                    |
