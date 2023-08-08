---
description: >-
  Follow this topic to activate your EA or MPSA Cloud Account for Azure or
  Office 365.
---

# Activating your EA or MPSA account

***

### Prerequisites <a href="#before-you-start" id="before-you-start"></a>

Before adding an account, make sure that you have the following details:

* **Account Information**: You must have the tenant ID or domain name of the tenant that contains your Azure or Office 365 subscriptions. The tenant ID and domain name are available in your Azure account. For information on how to find these details, see Locating your tenant ID or domain.
* **Permissions**: You must have sufficient permissions to complete the onboarding process. The setup will fail if the permissions are not configured in the [Microsoft Azure Portal](https://portal.azure.com/).
  * For an Azure account, you must have owner permission for the subscription you want to add.
  * For an Office 365 account, you must be a Global Administrator of the tenant that contains the subscriptions.

***

### **Activating your account**

**To activate your account**

1. From the main menu, navigate to **Setup** and select **Cloud Tenant Setup**.
2. On the Cloud Tenant Setup page, select **Add Cloud Account**.
3. On the Add Cloud Account page, select **Azure** or **Office 365** and provide the following details:
   1. A name for your Microsoft tenant.
   2. The tenant ID or tenant domain.
4. Select **Add Cloud Account**.
5. Sign in to the Microsoft portal using the credentials of a user who has Owner permissions to the Azure subscriptions you wish to add to PyraCloud.

{% hint style="info" %}
**NOTE:** If you wish to add more Azure subscriptions owned by other users, you can do this later. See the _Add more Subscriptions_ section later in this document.
{% endhint %}

6. On the consent page, review the permissions required by PyraCloud and select **Accept** to grant consent.&#x20;

You'll be redirected to the Cloud Tenant Setup page where you can view the new tenant and and its subscriptions. If the subscriptions are not immediately visible, wait a few minutes and refresh the page.

After activating your tenant, you can add subscriptions and allow PyraCloud to write tags back to your Azure resources.

***

### Adding an access token <a href="#add-an-access-token" id="add-an-access-token"></a>

**To add an access token**

1. On the Cloud Tenant Setup page, select **Manage** next to the tenant and select the **Access Tokens** tab.&#x20;
2. Select **Add Access Token**.
3. In **Add Access Token**, provide your new access token and select **Save**.

***

### Deleting an access token <a href="#delete-an-access-token" id="delete-an-access-token"></a>

**To delete an access token**

1. On the Cloud Tenant Setup page, expand the tenant and select **Access Tokens** tab.&#x20;
2. Select **Delete** next to the access token you wish to remove.
3. Select **Delete** to confirm deletion.

***

### Adding more Azure subscriptions <a href="#add-more-azure-subscriptions" id="add-more-azure-subscriptions"></a>

Many organizations have several Azure subscriptions in a single Microsoft tenant. In some cases, it is not always the same person who has Owner permissions on all those subscriptions. In such a case, it is necessary for each subscription owner to activate the subscriptions they own.

**To activate more subscriptions**

1. On the Cloud Tenant Setup page, select Manage next to the tenant you want to add more subscriptions from and select **Add Existing Subscriptions**.
2. In **Add New Subscription**, select the type of subscription and select **Add**.&#x20;

{% hint style="info" %}
If Azure is selected, then the user performing consent must be the Owner of the Azure subscriptions being added. If Office 365 is selected, then the user performing consent should be a Global Administrator of the tenant.
{% endhint %}

3. Sign in to the Microsoft portal using the credentials of the user who has Owner permissions to the Azure subscriptions you wish to add to PyraCloud.
4. On the consent page, review the permissions required by PyraCloud and select **Accept** to grant consent.

After granting consent, you'll be redirected to PyraCloud where you will see the subscriptions owned by the user added to PyraCloud.

***

### Syncing your tags to Azure

When you activate your Azure subscriptions for the first time, PyraCloud assigns the Reader role by default. This means that the Tags and Resources feature can import your resources and tags from Azure, but it cannot synchronize any tag changes you make in PyraCloud back to Azure.

If you would like Tags and Resources to synchronize tags back to Azure, you must to change the level of access PyraCloud has for your Azure subscription.

**To change the level of access PyraCloud has for an Azure subscription**

1. On the Cloud Tenant Setup page, select **Manage** and select **Change Access** next to the subscription you want to modify.
2. In **Change PyraCloud Access Level**, choose your desired access level and select **Change**. The following options are available:&#x20;
   * **Sync resources only, no tags – write back of tags disabled:** Tags and Resources will download your resources to PyraCloud without the tags currently assigned in Azure. Any changes to tags will be stored in PyraCloud only. This setting requires the “Reader” role in your Azure subscription and will not make any changes to resources or tags in your Azure subscription.
   * **Sync resources and tags – write back of tags disabled:** Tags and Resources will download your resources to PyraCloud including the tags currently assigned in Azure. Any changes to tags will be stored in PyraCloud only. Any tags assigned to resources in Azure will overwrite the tags for the corresponding resource in PyraCloud. This setting requires the “**Reader**” role in your Azure subscription and will not make any changes to resources or tags in your Azure subscription.
   * **Sync resources and tags – write back of tags enabled:** Tags and Resources will download your resources to PyraCloud including the tags currently assigned in Azure. Any changes to tags will be synchronized back to your resources in Azure. This setting requires the “Tag Contributor” role in your Azure subscription and will only make changes to tags.
3. Sign in to the Microsoft portal using the credentials of the user who has Owner permissions to the Azure subscriptions for which you wish to modify the PyraCloud access level.
4. On the consent page, review the permissions required by PyraCloud and select **Accept** to grant consent.&#x20;

After granting consent, you'll be redirected to PyraCloud where you can view the updated access level. If you notice a blank screen, refresh the page.&#x20;

***

### Generating your EA access token <a href="#generating-your-ea-access-token" id="generating-your-ea-access-token"></a>

Access tokens are generated through the Microsoft Azure Portal.&#x20;

To generate your access token, follow the steps in the following KB article: [How to Generate your Azure EA Access Token](https://help.pyracloud.com/knowledge-base/how-to-generate-your-ea-access-token/).

Save this access token for use during cloud account activation.

***

### Activating Azure Microsoft Customer Agreement (MCA) <a href="#activating-azure-microsoft-customer-agreement-mca" id="activating-azure-microsoft-customer-agreement-mca"></a>

PyraCloud supports both legacy EA and modern [MCA ](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/mca-overview)models. Before reading further please make sure you have followed [Activating your account](https://app.gitbook.com/o/sGLRSSUGgFSfUhFIYij8/s/B8rr5E9BB4HBPts7pBng/\~/changes/16/set-up/azure-onboarding/activating-your-ea-or-mpsa-account#activating-your-account).

#### To onboard your MCA tenant <a href="#how-to-onboard-mca-tenant" id="how-to-onboard-mca-tenant"></a>

1. Verify that your account has the proper billing account type set up. You can verify this in the [Azure Portal](https://portal.azure.com) > **Cost Management + Billing > Properties.**

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image.png" alt=""><figcaption></figcaption></figure>

2. Add the Billing Reader role to PyraCloud. To do so:
   1. Launch the [Azure Portal](https://portal.azure.com). Search for **Cost Management + Billing.**
   2. Select your MCA Billing Scope.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-7.png" alt="" height="301" width="643"><figcaption></figcaption></figure>

3. Select **Access Control (IAM)** to assign permissions.&#x20;

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-8.png" alt="" height="141" width="643"><figcaption></figcaption></figure>

4. Select **Add** and choose **Billing Account Reader** from the list of roles.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-9.png" alt="" height="255" width="627"><figcaption></figcaption></figure>

5. Select **Service Principle** in the select section of the panel.&#x20;

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2021/08/image-10.png" alt="" height="144" width="330"><figcaption></figcaption></figure>

6. Save your changes.&#x20;

After you save your changes, it takes approximately 24 hours for the MCA billing data to synchronize with PyraCloud.

***

### Locating your tenant ID or tenant Domain <a href="#locating-your-tenant-id-or-tenant-domain" id="locating-your-tenant-id-or-tenant-domain"></a>

To locate your Tenant ID or Tenant Domain, please follow the steps below:

1. Sign in to the Azure Portal at [https://portal.azure.com](https://portal.azure.com/). In the left navigation bar, click the **Azure Active Directory**. If you cannot view **Azure Active Directory**, then select **All Services** at the top-left, and locate the Azure Active Directory item under **Security + Identity**.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/word-image-59.png" alt=""><figcaption></figcaption></figure>

2. In **Azure Active Directory**, select **Properties**. Your Tenant ID is displayed in the **Directory ID** field. Copy or make a note of this ID for later use.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/word-image-60.png" alt=""><figcaption><p><strong>Figure 27 – Add Properties</strong></p></figcaption></figure>

3. In **Azure Active Directory**, select **Custom domain names**. Your domains are shown in a list. The required domain is the one marked primary. Copy or make a note of this for later use.

<figure><img src="https://help.pyracloud.com/wp-content/uploads/2019/10/word-image-61.png" alt=""><figcaption></figcaption></figure>

***

### Frequently Asked Questions <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

#### Why is my access token invalid? <a href="#why-is-my-access-token-invalid" id="why-is-my-access-token-invalid"></a>

An access token may be invalid for a few reasons:

* The token is not complete.
* The token is complete, but has expired
* The token is complete, but has been revoked

**The access token is incomplete**

If your access token is incomplete, log in to the Azure EA Portal and copy your access token again. To do this, follow steps 1 -6 and 9 and 10 in the Generating your EA Access Token section of this document.

**The access token is complete but has expired or has been revoked**

If your access token has expired or has been revoked, follow all the steps in the Generating your EA Access Token section of this document to generate a new access token.

#### What happens when I perform consent? <a href="#what-happens-when-i-perform-consent" id="what-happens-when-i-perform-consent"></a>

When you perform consent, you are redirect to Microsoft to accept permissions required by PyraCloud. As part of this process, PyraCloud is able to “impersonate” the consenting user for a short period (1 hour).

PyraCloud uses this impersonation to perform actions on behalf of the consenting user. This includes:

1. Assigning the Reader role to the PyraCloud application for subscriptions owned by the consenting user during onboarding. This is outlined in the Add your EA Microsoft Tenant and Subscriptions section of this document.
2. Assigning the Reader role to the PyraCloud application for subscriptions owned by the consenting user during the addition of more subscriptions to PyraCloud. This is outlined in the Add more subscriptions section of this document.
3. Modify the default Reader role to the Tag Contributor role (and vice versa) during the Change Access process. This is outlined in the Sync your tags to Azure section of this document.

#### What are the security implications of activating my tenant in PyraCloud? <a href="#what-are-the-security-implications-of-activating-my-tenant-in-pyracloud" id="what-are-the-security-implications-of-activating-my-tenant-in-pyracloud"></a>

When the consent process is performed, a “service principal” is created in your tenant. This is conceptually similar to adding a user dedicated to PyraCloud for the purposes of accessing your tenant and subscriptions.

**Azure Subscriptions**

When adding Azure subscriptions, the service principal is granted “Reader” access to those subscriptions. This is a built-in role in your Microsoft tenant that allows read only access to your resources. PyraCloud uses this access to retrieve a list of your resources (virtual machines, websites, etc.) and the tags assigned to them.

If you change the level of access to a setting that allows write back of tags, PyraCloud requires the “Tag Contributor” role. This level of access allows full access to your subscription with the notable exception of managing security settings in the subscription. PyraCloud uses this access to retrieve a list of your resources (virtual machines, websites, etc.) and the tags assigned to them. It also requires this level of access to synchronise the tags you assign in PyraCloud back to the resources your Azure subscription.

For more information, see the [Azure built-on roles reference](https://docs.microsoft.com/en-us/azure/active-directory/role-based-access-built-in-roles).

**Office 365 Subscriptions**

When adding Office 365 subscriptions, the service principal is granted permissions to the Microsoft Graph API in your Microsoft tenant. Those permissions include:

* **Read all usage report**s\
  Microsoft Description: Allows an app to read all service usage reports without a signed-in user. Services that provide usage reports include Office 365 and Azure Active Directory.
* **Read all groups**\
  Microsoft Description: Allows the app to read memberships for all groups without a signed-in user. Note that not all group API supports access using app-only permissions.
* **Read all user’s full profiles**\
  Microsoft Description: Allows the app to read the full set of profile properties, group membership, reports and managers of other users in your organization, without a signed-in user.

For more information, see the Microsoft Graph API permissions reference.
