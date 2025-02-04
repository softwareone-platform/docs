# Activate an Azure EA or MPSA Account

## Before you begin <a href="#before-you-start" id="before-you-start"></a>

Before adding an account, make sure that you have the following details:

* **Account Information -** You must have the tenant ID or domain name of the tenant that contains your Azure or Office 365 subscriptions. The tenant ID and domain name are available in your Azure account. For information on how to find these details, see [Find IDs and domain names](https://learn.microsoft.com/en-us/partner-center/find-ids-and-domain-names) in the Microsoft documentation.
* **Permissions -** You must have sufficient permissions to complete the onboarding process. The setup will fail if the permissions are not configured in the [Microsoft Azure Portal](https://portal.azure.com/).
  * For an Azure account, you must have owner permission for the subscription you want to add.
  * For an Office 365 account, you must be a **Global Administrator** of the tenant that contains the subscriptions.

## **Activate your cloud account**

Follow these steps to add a new cloud account to the Client Portal: &#x20;

1. On the [Cloud tenant setup](https://v1.client.softwareone.com/integration-manager/start) page (**Cloud tools** > **Cloud tenant setup**), click **Add Cloud Account**.
2. On the **Add Cloud Account** page, click **Azure** and provide the following details:
   1. **Friendly Name** - Provide a name for your Microsoft tenant.
   2. **Microsoft Tenant ID or Tenant Domain** - Provide the tenant ID or domain.
   3. **License Model** - Select the license model (**Enterprise Agreement** or **Microsoft Customer Agreement**).&#x20;
   4. **Enrollment Number** - Provide the enrollment number. Note that this field is displayed only if you select **Enterprise Agreement** as your license model.
3. Click **Add Cloud Account**.
4. Sign in to the Microsoft portal using the credentials of a user who has **Owner** permissions to the Azure subscriptions you want to add.

{% hint style="info" %}
If you wish to add more Azure subscriptions owned by other users, you can do this later. For instructions, see [Add more Azure Subscriptions](activate-an-azure-ea-or-mpsa-account.md#add-more-azure-subscriptions)_._
{% endhint %}

5. On the consent page, review the permissions required by the Client Portal and click **Accept** to grant consent.&#x20;

After clicking **Accept**, you'll be redirected to the **Cloud Tenant Setup** details page to view the new tenant and its activation progress. After activating your tenant, you can add subscriptions and allow the Client Portal to write tags back to your Azure resources.&#x20;

When you return to the Client Portal, you might see a blank page for a few seconds. To learn about the process that takes place after you provide consent, see [What happens after I grant consent.](../../../../help-and-support/faqs/i-have-questions-about-access-tokens-and-consent.md#what-happens-when-i-perform-consent)&#x20;

## Add more Azure subscriptions <a href="#add-more-azure-subscriptions" id="add-more-azure-subscriptions"></a>

Many organizations have several Azure subscriptions in a single Microsoft tenant. In some cases, it's not always the same person who has Owner permissions on all those subscriptions. In such cases, each subscription owner must activate their own subscriptions.

Follow these steps to add more subscriptions:

1. On the **Cloud Tenant Setup** page, click **Manage** and then select **Add Existing Subscriptions** to add more subscriptions.
2. In **Add New Subscription**, select the type of subscription and click **Add**.&#x20;
   * If you select **Azure**, the user performing consent must be the Owner of the Azure subscriptions being added.&#x20;
   * If you select **Office 365**, the user performing the consent must be a Global Administrator of the tenant.
3. Sign in to the Microsoft portal using the credentials of the user with Owner permissions to the Azure subscriptions you want to add.
4. On the consent page, review the permissions and click **Accept** to grant consent. After granting consent, you'll be redirected to the Client Portal.

## Sync your tags to Azure

When you activate your Azure subscriptions for the first time, the Client Portal assigns the **Reader** role by default. This means that the Tags and Resources feature can import your resources and tags from Azure, but it cannot synchronize any tag changes you make in the Client Portal back to Azure.

For Tags and Resources to synchronize tags back to Azure, you must change the level of access the Client Portal has for your Azure subscription.

Follow these steps to change the level of access:

1. On the **Cloud Tenant Setup** page, click **Manage.**
2. Click **Change Access** for the subscription you want to modify.
3. Select one of the following access levels and click **Change**:&#x20;
   * **Sync resources only, no tags – write back of tags disabled** - Tags and Resources will download your resources to the Client Portal without the tags currently assigned in Azure. Any changes to tags will be stored in the Client Portal only. This setting requires the “Reader” role in your Azure subscription and will not make any changes to resources or tags in your Azure subscription.
   * **Sync resources and tags – write back of tags disabled** - Tags and Resources will download your resources, including the tags currently assigned in Azure. Any changes to tags will be stored in the Client Portal only. Any tags assigned to resources in Azure will overwrite the tags for the corresponding resource in the Client Portal. This setting requires the **Reader** role in your Azure subscription and will not make any changes to resources or tags in your Azure subscription.
   * **Sync resources and tags – write back of tags enabled** - Tags and Resources will download your resources to the Client Portal including the tags currently assigned in Azure. Any changes to tags will be synchronized back to your resources in Azure. This setting requires the “Tag Contributor” role in your Azure subscription and will only make changes to tags.
4. Sign in to the Microsoft portal using the credentials of the user with Owner permissions to the Azure subscriptions for which you wish to modify the access level.
5. On the consent page, review the permissions and click **Accept** to grant consent. After granting consent, you'll be redirected to the Client Portal to view the updated access level. If you notice a blank screen, refresh the page.&#x20;
