---
description: Follow this topic to add your EA or MPSA cloud account to the Client Portal.
---

# Adding an Azure Enterprise Agreement (EA) Account

***

### Prerequisites <a href="#before-you-start" id="before-you-start"></a>

Before adding an account, make sure that you have the following details:

* **Account Information**: You must have the tenant ID or domain name of the tenant that contains your Azure or Office 365 subscriptions. The tenant ID and domain name are available in your Azure account. For information on how to find these details, see [Find IDs and domain names](https://learn.microsoft.com/en-us/partner-center/find-ids-and-domain-names) in the Microsoft documentation.
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
5. Sign in to the Microsoft portal using the credentials of a user who has Owner permissions to the Azure subscriptions you wish to add to the Client Portal.

{% hint style="info" %}
**NOTE:** If you wish to add more Azure subscriptions owned by other users, you can do this later. For instructions, see [Adding more Azure Subscriptions](adding-an-azure-enterprise-agreement-ea-account.md#add-more-azure-subscriptions)_._
{% endhint %}

6. On the consent page, review the permissions required by the Client Portal and select **Accept** to grant consent.&#x20;

After you grant consent, you'll be redirected to the Cloud Tenant Setup details page where you can view the new tenant and the activation progress. Note that when you return to the Client Portal, you may see a blank screen for a few seconds. To learn about the process that takes place after you provide consent, see [What happens after I grant consent?](../../../help-and-support/frequently-asked-questions/i-have-questions-about-access-tokens-and-consent.md#what-happens-when-i-perform-consent).&#x20;

After activating your tenant, you can add subscriptions and allow the Client Portal to write tags back to your Azure resources.

{% hint style="warning" %}
For Azure Only: After adding your cloud account, you must also add your EA access token.&#x20;
{% endhint %}

***

### Adding an access token <a href="#add-an-access-token" id="add-an-access-token"></a>

Access tokens are generated through the Microsoft Azure Portal. For information on how to generate a token, see [How to generate an Azure EA access token](../../../help-and-support/frequently-asked-questions/how-to-generate-an-azure-ea-access-token.md).

**To add your access token to the Client Portal**

1. On the Cloud Tenant Setup page, select **Manage** next to the tenant and select the **Access Tokens** tab.&#x20;
2. Select **Add Access Token**.
3. In **Add Access Token**, provide your new access token and select **Save**.

***

### Adding more Azure subscriptions <a href="#add-more-azure-subscriptions" id="add-more-azure-subscriptions"></a>

Many organizations have several Azure subscriptions in a single Microsoft tenant. In some cases, it is not always the same person who has Owner permissions on all those subscriptions. In such a case, it is necessary for each subscription owner to activate the subscriptions they own.

**To activate more subscriptions**

1. On the Cloud Tenant Setup page, select Manage next to the tenant you want to add more subscriptions from and select **Add Existing Subscriptions**.
2. In **Add New Subscription**, select the type of subscription and select **Add**.&#x20;

{% hint style="info" %}
**NOTE**: If Azure is selected, then the user performing consent must be the Owner of the Azure subscriptions being added. If Office 365 is selected, then the user performing consent should be a Global Administrator of the tenant.
{% endhint %}

3. Sign in to the Microsoft portal using the credentials of the user who has Owner permissions to the Azure subscriptions you wish to add to the Client Portal.
4. On the consent page, review the permissions and select **Accept** to grant consent.

After granting consent, you'll be redirected to PyraCloud where you will see the subscriptions owned by the user added to PyraCloud.

***

### Syncing your tags to Azure

When you activate your Azure subscriptions for the first time, PyraCloud assigns the Reader role by default. This means that the Tags and Resources feature can import your resources and tags from Azure, but it cannot synchronize any tag changes you make in PyraCloud back to Azure.

If you would like Tags and Resources to synchronize tags back to Azure, you must to change the level of access PyraCloud has for your Azure subscription.

**To change the level of access the Client Portal has for an Azure subscription**

1. On the Cloud Tenant Setup page, select **Manage** and select **Change Access** next to the subscription you want to modify.
2. In **Change PyraCloud Access Level**, choose your desired access level and select **Change**. The following options are available:&#x20;
   * **Sync resources only, no tags – write back of tags disabled:** Tags and Resources will download your resources to the Client Portal without the tags currently assigned in Azure. Any changes to tags will be stored in PyraCloud only. This setting requires the “Reader” role in your Azure subscription and will not make any changes to resources or tags in your Azure subscription.
   * **Sync resources and tags – write back of tags disabled:** Tags and Resources will download your resources to PyraCloud including the tags currently assigned in Azure. Any changes to tags will be stored in the Client Portal only. Any tags assigned to resources in Azure will overwrite the tags for the corresponding resource in PyraCloud. This setting requires the “**Reader**” role in your Azure subscription and will not make any changes to resources or tags in your Azure subscription.
   * **Sync resources and tags – write back of tags enabled:** Tags and Resources will download your resources to the Client Portal including the tags currently assigned in Azure. Any changes to tags will be synchronized back to your resources in Azure. This setting requires the “Tag Contributor” role in your Azure subscription and will only make changes to tags.
3. Sign in to the Microsoft portal using the credentials of the user who has Owner permissions to the Azure subscriptions for which you wish to modify the PyraCloud access level.
4. On the consent page, review the permissions and select **Accept** to grant consent.&#x20;

After granting consent, you'll be redirected to the Client Portal where you can view the updated access level. If you notice a blank screen, refresh the page.&#x20;

***
