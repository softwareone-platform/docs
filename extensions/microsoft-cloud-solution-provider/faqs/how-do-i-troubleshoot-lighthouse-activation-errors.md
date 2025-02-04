# How do I troubleshoot Lighthouse activation errors?

If you face an error during Lighthouse activation, it could be because of your role in Azure.&#x20;

Make sure that you are the owner of the subscription for which you are activating Lighthouse. Subscription owners have the **Azure Subscription Owner** role.

You can verify the role on the **Role assignments** tab in Azure.

<figure><img src="../../../.gitbook/assets/image-20241118-153405.png" alt=""><figcaption><p>Role assignments tab</p></figcaption></figure>

To complete the Lighthouse onboarding, you must also meet the following requirements for your primary domain/tenant or Azure subscription:

* **Role** - Any
* **User type** - Member
* **User principal name** - Must have no reference to 'external'
* **Identity** - Must match the tenant’s name for the partnership

<figure><img src="../../../.gitbook/assets/Untitled design (3).png" alt=""><figcaption><p>Entra ID Users Section</p></figcaption></figure>
