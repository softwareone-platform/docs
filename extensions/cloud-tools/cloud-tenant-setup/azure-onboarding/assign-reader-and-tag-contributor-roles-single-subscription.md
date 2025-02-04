# Assign Reader and Tag Contributor Roles (single subscription)

In some cases, you must configure your Azure subscription manually so that the Client Portal can access the resources and tags.&#x20;

When you onboard your tenant to the Client Portal, an Enterprise Application called PyraCloud (Azure) is created in your tenant. You must then assign the [Tag Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#tag-contributor) and [Reader](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#reader) roles to the PyraCloud (Azure) Enterprise Application.

These roles allow the Client Portal to read a list of all the resources in your Azure subscription, and read and write tags on those resources. You can control whether you want the Client Portal to write tags back to resources in your Azure subscription using the Cloud Tenant Setup feature.

## Grant access to individual subscriptions <a href="#block-e361c5ef-f066-4f15-882a-9691e45ebe2d" id="block-e361c5ef-f066-4f15-882a-9691e45ebe2d"></a>

{% hint style="info" %}
Before granting access, ensure that you've [onboarded your tenant](activate-an-azure-ea-or-mpsa-account.md).
{% endhint %}

Follow these steps to grant access:

1. Launch the [Azure Portal](https://portal.azure.com/#home) and search for **Subscriptions**.
2. On the **Subscriptions** page, choose the subscription you want to integrate with the Client Portal.

<figure><img src="../../../../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure>

3. Select **Access control (IAM).**

<figure><img src="../../../../.gitbook/assets/image (379).png" alt=""><figcaption></figcaption></figure>

4. Select the **Role assignments** tab.

<figure><img src="../../../../.gitbook/assets/image (380).png" alt=""><figcaption></figcaption></figure>

5. Click **Add** > **Add role assignment**.&#x20;

<figure><img src="../../../../.gitbook/assets/image (381).png" alt=""><figcaption></figcaption></figure>

6. Select **Reader** from the **Role** menu and then search for **Pyra**. Choose **PyraCloud (Azure)** and click **Save**.

<figure><img src="../../../../.gitbook/assets/image (382).png" alt=""><figcaption></figcaption></figure>

7. Select **Tag Contributor** from the **Role** menu and then search for **Pyra**. Choose **PyraCloud (Azure)** and select **Save**.

<figure><img src="../../../../.gitbook/assets/image (383).png" alt=""><figcaption></figcaption></figure>

The access is granted.&#x20;

<figure><img src="../../../../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure>
