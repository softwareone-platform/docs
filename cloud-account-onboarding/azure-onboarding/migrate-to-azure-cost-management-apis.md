---
description: Migrate from Azure Enterprise Reporting to Cost Management APIs.
---

# Migrate to Azure Cost Management APIs

Microsoft will retire the legacy Azure Enterprise Reporting APIs on 1 May 2024. Currently, the Client Portal uses these APIs to get your Azure EA consumption data.&#x20;

If you have an Azure Enterprise Agreement (EA), you must migrate to the new Azure Cost Management APIs to maintain your cost and usage data in the Client Portal.&#x20;

## Before you begin

Before migrating to the new Cost Management APIs, note the following points:

* The new APIs don't require access tokens because the authorization is done through Microsoft Entra ID (also known as Azure Active Directory) using service principals.&#x20;
* Only individuals with the **Azure EA Enterprise Administrator** role permission can carry out the migration steps. If you have trouble finding out who is your EA admin in Azure, see Microsoft's documentation on [EA Billing administration on the Azure portal](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/direct-ea-administration#add-another-enterprise-administrator).&#x20;
* If your EA admin doesn't have access to the Client Portal, you can collaborate with them by sharing your screen, so that your EA admin can sign in and complete the authorization required for migration.&#x20;
* During migration, our system will automatically assign the [EnrollmentReader role permission](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/assign-roles-azure-service-principals#permissions-that-can-be-assigned-to-the-service-principal) to the service principal.&#x20;

## Migrate your existing EA cloud account

If you've already onboarded your EA cloud account to the Client Portal, follow these steps to transition to the new API:

1. Open the [Cloud Tenant Setup](https://v1.client.softwareone.com/integration-manager/start) page. The EA cloud accounts that haven't been migrated will display **EA API migration required** in the **Status** column.

<figure><img src="../../.gitbook/assets/image (292).png" alt="" width="563"><figcaption><p>Status column displays EA API migration required</p></figcaption></figure>

2. Click **Migrate EA API**.&#x20;
3. In the **Migrate to EA API** window, enter the enrollment number and click **Migrate**.&#x20;

<figure><img src="../../.gitbook/assets/image (296).png" alt="" width="428"><figcaption></figcaption></figure>

4. Sign in to the Microsoft portal using the credentials of a user with **Enterprise administrator** permission.
5. On the consent page, review the permissions required by the Client Portal and click **Accept** to grant consent.

<figure><img src="../../.gitbook/assets/image (294).png" alt="" width="338"><figcaption><p>Permissions and consent</p></figcaption></figure>

After clicking **Accept**, you'll be redirected to the Cloud Tenant Setup details page.&#x20;

The system will mark the enrollment number you provided as migrated, and automatically assign the **Enrollment reader** permission to the PyraCloud (Azure) application. When the migration is completed, the consumption data will be fetched from Microsoft.

{% hint style="info" %}
**Migration did not complete successfully?**&#x20;

If the migration fails despite following these steps, you can use the fallback option to complete the process.&#x20;

To do so, go to the **Enrollment Numbers** tab of the tenant and click **Show manual steps** in the **Actions** column. When the **Manual steps** dialog opens, execute the commands and then click **Close**.&#x20;

If you are still unable to migrate, contact your support team.
{% endhint %}

### Enrollment statuses

The **Enrollment Numbers** tab on the details page of the cloud tenant displays the enrollment numbers that are migrated to the new API, along with the respective enrollment status:

<figure><img src="../../.gitbook/assets/Enrollment Numbers (1).png" alt=""><figcaption><p>Enrollment Numbers tab</p></figcaption></figure>

* **Connected** - Indicates that the system is connected and working as expected.
* **Cannot Connect** - Indicates that the Client Portal doesn't have access to the new Azure Cost Management API and the **EnrollmentReader** permission is missing. You can assign permissions using the Azure Cost Management API or Azure Cloud Shell.
* **Activation Required** - Indicates that the Client Portal can access the enrollment data, but the cloud account has not been set up as an EA account type.

## Add a new EA cloud account <a href="#user-content-adding-a-new-ea-cloud-account" id="user-content-adding-a-new-ea-cloud-account"></a>

If you're adding a new EA cloud account to the Client Portal, you'll need to provide the enrollment number while adding the account. For information on how to add a new EA account, see [Activate your cloud account](activate-an-azure-ea-or-mpsa-account.md#activate-your-cloud-account).
