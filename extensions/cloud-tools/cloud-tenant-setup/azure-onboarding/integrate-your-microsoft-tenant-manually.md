# Integrate Your Microsoft Tenant Manually

This topic describes how to manually integrate your Azure tenant and assign the Reader and Tag Contributor roles to the Client Portal using Azure Management Groups.&#x20;

Integrating a Microsoft tenant involves the following steps:

1. Granting consent to the Client Portal in your Azure tenant.
2. Assigning the [Tag Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor) and [Reader](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#reader) access roles to the Client Portal using Azure Management Groups. The **Tag Contributor** and **Reader** roles allow the Client Portal to read a list of all the resources in your Azure subscription, and read and write tags on those resources. You can control whether you want the Client Portal to write tags back to resources in your Azure subscription. For more information, see [Syncing your tags to Azure](activate-an-azure-ea-or-mpsa-account.md#syncing-your-tags-to-azure).
3. Providing the details to SoftwareOne to complete your onboarding.

## Granting consent through your Azure tenant <a href="#providing-consent-to-pyracloud-in-your-azure-tenant" id="providing-consent-to-pyracloud-in-your-azure-tenant"></a>

Follow these steps to grant consent through your Azure tenant:

1. Select one of the following links:
   * [Azure](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code\&client_id=2a4807a4-d9e4-457d-b32f-a455e0d3662a\&prompt=consent\&redirect_uri=https://www.softwareone.com/)
   * [Office365](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code\&client_id=3f18953a-acbf-48cf-b485-06e451411aef\&prompt=consent\&redirect_uri=https://www.softwareone.com/)
2. On the **Permissions Requested** page, review the permissions, and select **Accept**.
3. After granting consent, launch the Azure Portal and navigate to **Azure Active Directory** > **Enterprise applications** to make sure that SoftwareOne Cloud Consumption (formerly PyraCloud) is listed in your enterprise applications.

## Assigning the Tag Contributor and Reader access roles   <a href="#granting-access-to-pyracloud-with-azure-management-groups" id="granting-access-to-pyracloud-with-azure-management-groups"></a>

Follow these steps to assign the Tag Contributor and Reader access roles:

1. Launch the [Azure Portal](https://portal.azure.com/) and search for **Management groups**.
2. On the **Management groups** page, select **Start using management groups**.
3. Provide the Group ID and a display name for your group. Select **Submit**. The new group is created and displayed under the Tenant Root Group.
4. Select the newly created management group and then from the left sidebar, select **Access Control (IAM)**.
5. Navigate to **Role assignments** and select **Add > Add role assignment** from the dropdown.
6. Assign the Reader role to the Client Portal:
   1. Choose **Reader** from the list of roles and select **Next**.
   2. On the **Members** tab, click **Select Members**.
   3. Search for **SoftwareOne Cloud Consumption** (formerly _PyraCloud Azure_ for Azure or _PyraCloud Office 365_ for Office 365) and then select it from the search results. Click **Save**.
7. Assign the Tag Contributor role to the Client Portal:
   1. Choose **Tag Contributor** from the list of roles. Select **Next**.
   2. On the **Members** tab, click **Select Members**.
   3. Search for **SoftwareOne Cloud Consumption** (formerly _PyraCloud Azure_ for Azure or _PyraCloud Office 365_ for Office 365) and then select it from the search results. Click **Save**.
8. Select **Review + assign** and then **Review + assign** again. The new roles are displayed on the page.

## Providing the details to SoftwareOne <a href="#providing-details-to-softwareone" id="providing-details-to-softwareone"></a>

After completing the integration steps, provide the following details so we can complete the onboarding of your tenant:

* Your Microsoft Tenant ID (or domain).
* A friendly name for your tenant to recognize easily across the Client Portal.
* The start and end date of your Enterprise Agreement.

After we have added your tenant, you'll need to provide an access token from the EA Portal.&#x20;

<details>

<summary>Removing the Azure role assignment</summary>

The Reader role is mandatory for all consumption modules including Reporting, Budgeting, Resources, and Tag Management.

The Tag Contributor role is required for the Client Portal to write back resource tagging information to the publisher (Azure). It is recommended to grant such a role to have consistent resource tag representation between Azure and the Client Portal. However, the Tag Contributor role can be revoked and the Client Portal will use Virtual Tags that will be visible only in the module.

However, the Tag Contributor role can be revoked and the Client Portal will use Virtual Tags that will be visible only in the module.

**To remove the Tag Contributor role**

1. Go to the scope where the role was granted (Subscription, Management Groups, or Root Management Group).
2. From the left sidebar, select **Access control (IAM)** and go to the **Role assignments** tab.
3. Choose the role that you want to remove and select **Remove**.
4. Select **Yes** to confirm the role removal.

</details>
