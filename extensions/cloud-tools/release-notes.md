---
description: Learn what's new and improved in Client Portal's Azure Cloud Spend Management.
---

# Release Notes

**Release Date: 22 April 2024**

## New Azure Cost Management APIs

On 1 May 2024, Microsoft will retire the legacy Azure Enterprise Reporting (EA) APIs. Currently, the Client Portal uses these APIs to get your Azure EA consumption data.

If you have an Azure Enterprise Agreement, you must migrate to the new Azure Cost Management APIs to maintain your cost and usage data in the Client Portal.&#x20;

For instructions on migrating to the new APIs, see [Migrate to Azure Cost Management APIs](cloud-tenant-setup/azure-onboarding/migrate-to-azure-cost-management-apis.md).&#x20;

You can also see Microsoft's documentation on [Migrate from Azure Enterprise Reporting to Microsoft Cost Management APIs overview.](https://learn.microsoft.com/en-us/azure/cost-management-billing/automate/migrate-ea-reporting-arm-apis-overview)

## Changes to the Cloud Tenant Details page <a href="#user-content-cloud-tenant-setup-changes" id="user-content-cloud-tenant-setup-changes"></a>

In the cloud tenant's details page, the **Access Tokens** tab has been replaced by a new tab called **Enrollment Numbers**.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Enrollment Numbers tab</p></figcaption></figure>

This change is made because the new Azure Cost Management APIs don't require access tokens. Instead, they use Microsoft Entra ID (also known as Azure Active Directory) for authentication.

On the **Enrollment Numbers** tab, you can view all enrollment numbers that are migrated to the new API, along with the enrollment status. For possible statuses and their description, see [Enrollment statuses](cloud-tenant-setup/azure-onboarding/migrate-to-azure-cost-management-apis.md#enrollment-statuses).

## Azure Savings Plans in the Client Portal

Clients who have a Microsoft CSP subscription through SoftwareOne and commit to an Azure Saving Plan can now see their savings plan cost in the Client Portal.&#x20;

<figure><img src="../../.gitbook/assets/image (295).png" alt="" width="563"><figcaption><p>Savings plan visibility</p></figcaption></figure>

To support this update, the following changes are made:

* Each savings plan has a details page that shows resource details. You can access the details page by clicking the savings plan on the **Resources** page.
* A new subscription type called **Savings Plans** and a new resource type called **Savings Plan Order** is added, making it easy for you to search for your savings plan resources.
* New filters and dimensions specific to Azure savings plans are added so you can break down your data. You can find the new filters and dimensions on various reporting and analytics pages in the Client Portal.&#x20;
