---
description: Administrators can enable the software assets integration.
---

# Software Assets

***

The Software Assets module allows you to manage your software assets and inventory for software purchased through SoftwareOne.

To access the Software Assets module, navigate to the main menu of the Client Portal and then select **Inventory** > **Software Assets**.

Watch the following video tutorial on how to use Software Assets:

{% embed url="https://vimeo.com/904502651" %}

***

## Enabling software assets <a href="#configuring-software-assets-integration" id="configuring-software-assets-integration"></a>

Only administrators can enable the Software Assets module.

**To enable the module**

1. From the main menu of the Client Portal, navigate to **Setup** and select **Cloud Tenant Setup**.
2. On the Cloud Tenant Setup page, select **Activate** from the **Actions** column. Note that the Software Assets row is only visible to the administrator accounts.

Once you've activated Software Assets, your activated account will be visible in the Resources, Budgets, and Consumption modules within 24 hours.

***

## Disabling software assets&#x20;

Once the Software assets module is enabled, you can control transaction filtering or disable the module.&#x20;

{% hint style="warning" %}
Take caution when disabling Software Assets. You can always enable it again, however, all transaction allocation and tag assignments must be redone.
{% endhint %}

To disable Software Assets, navigate to the **Cloud Tenant Setup** page and then select **Manage** from the Actions column.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

When the Software Assets page opens, select **Disable Software Assets.** When the feature is disabled, your software assets are removed from the Resource Manager, Budgets, Custom Group Manager, Chargebacks, and Consumption modules.

<figure><img src="../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

Note that by default, the filtering option is selected. It means that transactions relating to Azure or O365 will not be visible in the Resources, Budgets, and Consumption modules. Any changes to filtering settings take effect after 24 hours.

***

## Viewing your software assets and financial transactions

You can view your active software subscriptions, current spending, or your entire spending including subscriptions.

**To view your software assets and financial transactions**

1. From the main menu of the Client Portal, navigate to **Inventory** and select **Software Assets**.
2. Use the search options to view your software asset inventory list. You can either enter your PO number or reference number in the **Reference** field or use the filters to narrow down the search results.
3. Review the details on the **Software Assets** and **Financial Transactions** tabs.
   * The **Software Assets** tab displays your active software subscriptions and current spend only. It does not display your past payments.&#x20;
   * The **Financial Transactions** tab displays your entire spending across all software, including subscriptions and your past transactions.

***

## Exporting your software asset inventory list

The **Export** option on the Software Assets page allows you to export your software asset inventory list to several formats. The export templates allow you to export the software asset data in the most commonly configured format (column namings/order) for several Software Asset Management (SAM) tools, such as:

* Aspera
* Miss Marple
* Snow
* Flexera
* Service Now

Depending on your SAM Tool setup, you may need to amend the standard reporting templates. To learn more about the reporting templates, see [Reports](../../analytics-and-reports/reports/).

From the **Exports** menu, you can also export your Assets Default, Financial Statement, and Customer License Statement to various formats.

***

## Importing your software assets

You can use our Import templates to import your software assets to the Client Portal.

{% hint style="info" %}
To add items and contracts that haven't been purchased through SoftwareOne to the Client Portal, contact us to find out about our Entitlement Management Services.
{% endhint %}

**To import your software assets**

1. Download the import template. The following templates are available:

{% file src="../../.gitbook/assets/Activation-Key-Import-Template.xlsx" %}
Activation Key Import Tempate
{% endfile %}

{% file src="../../.gitbook/assets/Contract-Import-Template.xlsx" %}
Contract Import Template
{% endfile %}

{% file src="../../.gitbook/assets/Inventory-Import-Template (3).xls" %}
Inventory Import Template
{% endfile %}

2\. Fill the required data and email the file to your SoftwareOne Account Manager.&#x20;

Our team will validate the data and upload the file when the validation is completed. Note that the processing time might vary depending on the amount of data.
