---
description: >-
  Find answers to commonly asked questions regarding access tokens and granting
  consent.
---

# I have questions about access tokens and consent

***

### Why is my access token invalid? <a href="#why-is-my-access-token-invalid" id="why-is-my-access-token-invalid"></a>

An access token may be invalid due to the following reasons:

* The token is incomplete: If your access token is incomplete, sign in to the Azure EA Portal and copy your access token again.&#x20;
* The token is complete but it has expired: If your access token has expired, you must generate a new token.
* The token is complete but it has been revoked: If your access token has been revoked, you must generate a new token.

***

### What happens after I grant consent? <a href="#what-happens-when-i-perform-consent" id="what-happens-when-i-perform-consent"></a>

When you perform consent, you are redirected to Microsoft to accept permissions required by PyraCloud. As part of this process, PyraCloud is able to “impersonate” the consenting user for a short period (1 hour).

PyraCloud uses this impersonation to perform actions on behalf of the consenting user. This includes:

1. Assigning the Reader role to the PyraCloud application for subscriptions owned by the consenting user during onboarding.&#x20;
2. Assigning the Reader role to the PyraCloud application for subscriptions owned by the consenting user during the addition of more subscriptions to PyraCloud. For more information, see [Adding more subscriptions](../../cloud-account-onboarding/azure-onboarding/adding-an-azure-enterprise-agreement-ea-account.md#add-more-azure-subscriptions).
3. Modify the default Reader role to the Tag Contributor role (and vice versa) during the Change Access process. For more information, see [Sync your tags to Azure](../../cloud-account-onboarding/azure-onboarding/adding-an-azure-enterprise-agreement-ea-account.md#syncing-your-tags-to-azure).

***

### What are the security implications of activating my tenant in the Client Portal? <a href="#what-are-the-security-implications-of-activating-my-tenant-in-pyracloud" id="what-are-the-security-implications-of-activating-my-tenant-in-pyracloud"></a>

When the consent process is performed, a “service principal” is created in your tenant. This is conceptually similar to adding a user dedicated to PyraCloud for the purposes of accessing your tenant and subscriptions.

#### **Azure Subscriptions**

When adding Azure subscriptions, the service principal is granted “Reader” access to those subscriptions. This is a built-in role in your Microsoft tenant that allows read-only access to your resources. PyraCloud uses this access to retrieve a list of your resources (virtual machines, websites) and the tags assigned to them.

If you change the level of access to a setting that allows the write-back of tags, PyraCloud requires the “Tag Contributor” role. This level of access allows full access to your subscription with the notable exception of managing security settings in the subscription. PyraCloud uses this access to retrieve a list of your resources (virtual machines, websites, etc.) and the tags assigned to them. It also requires this level of access to synchronize the tags you assign in PyraCloud back to the resources of your Azure subscription.

For more information, see [Microsoft documentation - Azure built-on roles reference](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).

#### **Office 365 Subscriptions**

When adding Office 365 subscriptions, the service principal is granted permission to the Microsoft Graph API in your Microsoft tenant. Those permissions include:

* **Read all usage reports:** Allows an app to read all service usage reports without a signed-in user. Services that provide usage reports include Office 365 and Azure Active Directory.
* **Read all groups:** Allows the app to read memberships for all groups without a signed-in user. Note that not all group API supports access using app-only permissions.
* **Read all users’ full profiles**: Allows the app to read the full set of profile properties, group membership, reports, and managers of other users in your organization, without a signed-in user.

For more information, see the Microsoft Graph API permissions reference.
