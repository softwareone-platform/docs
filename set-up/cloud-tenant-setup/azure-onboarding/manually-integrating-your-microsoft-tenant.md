---
description: Learn how to integrate your Microsoft tenant.
---

# Manually integrating your Microsoft tenant

***

This topic describes how you can integrate your Microsoft tenant with PyraCloud. The integration involves the following steps:

1. Granting consent to PyraCloud in your Azure tenant.
2. Using the Azure Management Groups to assign the [Tag Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor) and [Reader](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#reader) access roles to PyraCloud.
3. Sharing the details to SoftwareOne so we can complete your onboarding.

The Tag Contributor and Reader roles allow PyraCloud to read a list of all the resources in your Azure subscription, and read and write tags on those resources. You can control whether PyraCloud will write tags back to resources in your Azure subscription. For more information, see Sync Your Tags to Azure.

***

### Providing consent to PyraCloud in your Azure tenant <a href="#providing-consent-to-pyracloud-in-your-azure-tenant" id="providing-consent-to-pyracloud-in-your-azure-tenant"></a>

**To grant consent**

1. Select one of the following links:
   * [Azure](https://login.microsoftonline.com/common/oauth2/authorize?response\_type=code\&client\_id=2a4807a4-d9e4-457d-b32f-a455e0d3662a\&prompt=consent\&redirect\_uri=https://www.softwareone.com/)
   * [Office365](https://login.microsoftonline.com/common/oauth2/authorize?response\_type=code\&client\_id=3f18953a-acbf-48cf-b485-06e451411aef\&prompt=consent\&redirect\_uri=https://www.softwareone.com/)

2\. On the **Permissions Requested** page, review the permissions, and select **Accept** to grant consent.

3\. After granting consent, launch the Azure Portal and navigate to **Azure Active Directory** > **Enterprise applications**. This step is necessary to ensure that PyraCloud is listed in your enterprise applications.

***

### Granting access to PyraCloud with Azure Management Groups <a href="#granting-access-to-pyracloud-with-azure-management-groups" id="granting-access-to-pyracloud-with-azure-management-groups"></a>

**To grant access to PyraCloud with Azure Management Groups:**

1. Launch the [Azure Portal](https://portal.azure.com/) and search for **Management groups**.
2. On the **Management groups** page, select **Start using management groups**.
3. Provide the Group ID and a display name for your group. Select **Submit**. The new group will be created and displayed under the Tenant Root Group.
4. Select the newly created management group and then from the left sidebar, select **Access Control (IAM)**.
5. Navigate to **Role assignments** and select **Add > Add role assignment** from the dropdown.
6. Assign the Reader role to PyraCloud:
   1. Choose **Reader** from the list of roles and select **Next**.
   2. On the **Members** tab, click on **Select Members,** and then in the **Search** box, type **PyraCloud**.
   3. From the search results, choose **PyraCloud (Azure)** for Azure or **PyraCloud (Office 365)** for Office 365. Select **Save**.
7. Assign the Tag Contributor role to PyraCloud:
   1. Choose **Tag Contributor** from the list of roles. Select **Next**.
   2. On the **Members** tab, click on **Select Members,** and then in the **Search** box, type **PyraCloud**.
   3. From the search results, choose **PyraCloud (Azure)** for Azure or **PyraCloud (Office 365)** for Office 365. Select **Save**.
8. Select **Review + assign** and then **Review + assign** again.

The new roles will be displayed on the page.

***

### Providing details to SoftwareOne <a href="#providing-details-to-softwareone" id="providing-details-to-softwareone"></a>

After you’ve completed the integration steps, provide the following details so that we can complete the onboarding of your tenant:

* Your Microsoft Tenant ID (or domain).
* A friendly name for your tenant to recognize easily across PyraCloud.
* The start and end date of your Enterprise Agreement.

After we’ve added your tenant, you will also need to provide an access token from the EA Portal. For information on how to provide an access token, see Add an Access Token.

***

### Removing the Azure role assignment <a href="#removing-the-azure-role-assignment" id="removing-the-azure-role-assignment"></a>

The Reader role is mandatory for all consumption modules including Reporting, Budgeting, Resources, and Tag Management.

The Tag Contributor role is required for PyraCloud to write back resource tagging information to the publisher (Azure). It is recommended to grant such a role to have consistent resource tag representation between Azure and PyraCloud. However, the Tag Contributor role can be revoked and PyraCloud will use Virtual Tags that will be visible only in the PyraCloud module

However, the Tag Contributor role can be revoked and PyraCloud will use Virtual Tags that will be visible only in the PyraCloud module.

**To remove the Tag Contributor role**

1. Go to the scope where the role was granted (Subscription, Management Groups, or Root Management Group).
2. From the left sidebar, select **Access control (IAM)** and go to the **Role assignments** tab.
3. Choose the role that you want to remove and select **Remove**.
4. Select **Yes** to confirm the role removal.
