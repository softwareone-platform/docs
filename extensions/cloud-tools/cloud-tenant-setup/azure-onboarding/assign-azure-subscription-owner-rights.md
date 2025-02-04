# Assign Azure Subscription Owner Rights

As a Global Administrator, you can manage all Azure subscriptions and management groups in your tenant by elevating your access.&#x20;

When you elevate your access, you'll be assigned the [User Access Administrator](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles#user-access-administrator) role in Azure at root scope (`/`).  This allows you to view all resources and assign access to any subscription or management group in the directory.&#x20;

To elevate access, follow the instructions in Microsoft documentation: [Elevate access to manage all Azure subscriptions and management groups](https://learn.microsoft.com/en-us/azure/role-based-access-control/elevate-access-global-admin?tabs=azure-portal), or perform these steps:

1. Sign in to Azure Portal as a Global Administrator.
2. Open **Microsoft Entra ID**. You can use the Azure search bar to find **Microsoft Entra ID**.

<figure><img src="../../../../.gitbook/assets/Microsoft Entra ID (1).png" alt="" width="563"><figcaption><p>Microsoft Entra ID</p></figcaption></figure>

3. Under **Manage**, select **Properties**.

<figure><img src="../../../../.gitbook/assets/image (1052).png" alt=""><figcaption><p>Properties</p></figcaption></figure>

4. Under **Access management for Azure resources**, set the toggle to **Yes**.

{% hint style="info" %}
This toggle is only available to users who are assigned the Global Administrator role in Microsoft Entra ID.
{% endhint %}

<figure><img src="../../../../.gitbook/assets/image (1053).png" alt=""><figcaption><p>Toggle under Access Management for Azure Resources.</p></figcaption></figure>

5. Click **Save**. This will grant you permission to assign roles in all Azure subscriptions and management groups associated with this Microsoft Entra ID.
6. If required, sign out and sign back in to refresh your permissions.
