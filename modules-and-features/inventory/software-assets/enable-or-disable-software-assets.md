# Enable or Disable Software Assets

{% hint style="info" %}
Before enabling or disabling the module, note the following points:

* Only administrators can enable or disable the module.
* Take caution when disabling the module. You can always enable it again, but you'll need to redo all transaction allocation and tag assignments.
{% endhint %}

## Enable software assets

Follow these steps to enable the module:

1. Sign in to your account as an account administrator.
2. From the main menu of the Client Portal, navigate to **Setup** > **Cloud Tenant Setup**.
3. On the **Cloud Tenant Setup** page, click **Activate** in the **Actions** column.&#x20;

After you've activated the module, your activated account will be visible in the other Cloud modules (such as Budgets, Resources, Chargebacks, and Consumption) within 24 hours.

## Disable software assets&#x20;

Follow these steps to deactivate the module:

1. Navigate to the **Cloud Tenant Setup** page.
2. In the **Actions** column, click **Manage**.

<figure><img src="../../../.gitbook/assets/image (796).png" alt=""><figcaption><p>Cloud Tenant Setup page</p></figcaption></figure>

3. Click **Disable Software Assets**. Your software assets are removed from all the Cloud modules.&#x20;

<figure><img src="../../../.gitbook/assets/image (795).png" alt=""><figcaption><p>Disable Software Assets option</p></figcaption></figure>

Note that the **Remove duplicate transactions** option is enabled by default. It means that transactions relating to Azure or Office 365 won't be visible in the Resources, Budgets, and Consumption modules. If you disable the option, the changes take effect after 24 hours.

## Related topics

{% content-ref url="./" %}
[.](./)
{% endcontent-ref %}

{% content-ref url="view-software-assets.md" %}
[view-software-assets.md](view-software-assets.md)
{% endcontent-ref %}

{% content-ref url="export-software-assets.md" %}
[export-software-assets.md](export-software-assets.md)
{% endcontent-ref %}

{% content-ref url="import-software-assets.md" %}
[import-software-assets.md](import-software-assets.md)
{% endcontent-ref %}
