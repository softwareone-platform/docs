---
description: >-
  Use Azure Management Group to assign permissions across multiple subscriptions
  in a single step.
---

# Assigning Reader and Tag Contributor Roles (Multiple Subscriptions)

***

You can use Azure Management Groups to grant the Client Portal access to your Azure subscriptions. This approach has the following benefits:&#x20;

* You can assign access to multiple subscriptions in a single step.
* If you create more Azure subscriptions in the future, the access will be automatically granted. It means when you add an Azure subscription to your tenant, there is no need to activate it in the Client Portal.

***

### How does it work?

When you onboard your tenant to the Client Portal, an Enterprise Application called "PyraCloud (Azure)" is created in your tenant. You must then assign the [Tag Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor) and [Reader](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#reader) roles to the "PyraCloud (Azure)" Enterprise Application:

These roles allow the Client Portal to read a list of all the resources in your Azure subscriptions, and read and write tags on those resources. You can choose whether you want the Client Portal to write tags back to resources in your Azure subscription using the Cloud Tenant Setup feature.

***

***

## Granting access using the Azure CLI

#### Prerequisites

* Ensure that you've installed PowerShell and Azure CLI. For installation instructions, see [Install PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell) and [Install Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).

**To onboard your Azure subscriptions**

* Use the following commands:

{% hint style="warning" %}
You must execute this script at a PowerShell prompt and not a normal command prompt because the script utilizes PowerShell variables.
{% endhint %}

<pre class="language-powershell" data-overflow="wrap" data-full-width="false"><code class="lang-powershell">az login

<a data-footnote-ref href="#user-content-fn-1">az rest --method post --url "/providers/Microsoft.Authorization/elevateAccess?api-version=2016-07-01"</a>

az ad sp create --id 2a4807a4-d9e4-457d-b32f-a455e0d3662a

az ad app permission grant --id 2a4807a4-d9e4-457d-b32f-a455e0d3662a --api 00000003-0000-0000-c000-000000000000 --scope "User.Read"

$root_mg=$(az account management-group list --query "[?displayName == 'Tenant Root Group'] | [0] | id" --output tsv)

az role assignment create --assignee "2a4807a4-d9e4-457d-b32f-a455e0d3662a" --role "Reader" --scope "$root_mg"

az role assignment create --assignee "2a4807a4-d9e4-457d-b32f-a455e0d3662a" --role "Tag Contributor" --scope "$root_mg"
</code></pre>

The following table explains these commands:

<table><thead><tr><th width="448">Command</th><th>Description</th></tr></thead><tbody><tr><td><code>az login</code></td><td>Log in to your Microsoft tenant.</td></tr><tr><td><code>az rest --method post --url "/providers/Microsoft.Authorization/elevateAccess?api-version=2016-07-01"</code></td><td>Elevate your permissions to manage all Azure subscriptions and management groups. See <a href="https://docs.microsoft.com/en-us/azure/role-based-access-control/elevate-access-global-admin">Microsoft Documentation</a>.</td></tr><tr><td><p><code>az ad sp create --id 2a4807a4-d9e4-457d-b32f-a455e0d3662a</code></p><p></p><p><code>az ad app permission grant --id 2a4807a4-d9e4-457d-b32f-a455e0d3662a --api 00000003-0000-0000-c000-000000000000 --scope "User.Read"</code></p></td><td>Create the PyraCloud (Azure) service principal (Enterprise Application) in your tenant.</td></tr><tr><td><code>$root_mg=$(az account management-group list --query "[?displayName == 'Tenant Root Group'] | [0] | id" --output tsv)</code></td><td>Get the ID of your Tenant Root Group.</td></tr><tr><td><p><code>az role assignment create --assignee "2a4807a4-d9e4-457d-b32f-a455e0d3662a" --role "Reader" --scope "$root_mg"</code></p><p></p><p><code>az role assignment create --assignee "2a4807a4-d9e4-457d-b32f-a455e0d3662a" --role "Tag Contributor" --scope "$root_mg"</code></p></td><td>Assign the Reader and Tag Contributor roles to the PyraCloud (Azure) application in your Tenant Root Group.</td></tr></tbody></table>

***

## Granting access using the Azure Portal

#### Prerequisites

* Ensure that you've [onboarded your tenant](adding-an-azure-enterprise-agreement-ea-account.md).
* Ensure that have the correct permissions to manage access to all Azure subscriptions and management groups in your tenant. For instructions, see [Elevate access to manage all Azure subscriptions and management groups](https://learn.microsoft.com/en-us/azure/role-based-access-control/elevate-access-global-admin) in the Microsoft documentation.&#x20;

**To grant access to PyraCloud**

1. Sign in to the [Azure Portal](https://portal.azure.com/#home) and search for **Management groups**.
2. On the **Management groups** page, select **Tenant Root Group**.

{% hint style="info" %}
**NOTE**: Regardless of your organization's configuration, a Tenant Root Group. This may have been renamed, but will always appear at the top of the hierarchy.
{% endhint %}

3. From the left sidebar, select **Access control (IAM).**
4. Navigate to **Role Assignments** and select **Add > Add role assignment** from the dropdown.
5. In Add Role Assignment, assign the Reader role to PyraCloud:
   1. Choose **Reader** from the list of roles.
   2. In **Select,** type **Pyra** and select **PyraCloud (Azure)** from the search results.&#x20;
   3. Select **Save**.
6. In Add Role Assignment, assign the Tag Contributor role to PyraCloud:
   1. Choose **Tag Contributor** from the list of roles.
   2. In **Select,** type **Pyra** and select **PyraCloud (Azure)** from the search results.&#x20;
   3. Select **Save**.

The access is granted:&#x20;

<figure><img src="../../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>



[^1]: 
