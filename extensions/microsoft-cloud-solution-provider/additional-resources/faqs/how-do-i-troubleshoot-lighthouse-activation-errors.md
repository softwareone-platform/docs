# How do I troubleshoot Lighthouse activation errors

If you face an error when onboarding subscriptions to Azure Lighthouse, it could be due to your role within Azure.

Make sure you are the owner of the subscription you wish to onboard and the first subscription that was onboarded to Azure Lighthouse. Subscription owners have the **Azure Subscription Owner** role, which can be verified on the **Role Assignments** tab within Azure.&#x20;

During onboarding, the initial subscription is highlighted so you can identify it.

<figure><img src="../../../../.gitbook/assets/image-20241118-153405.png" alt=""><figcaption><p>The Role assignments tab.</p></figcaption></figure>

To complete the Lighthouse onboarding, you must also meet the following requirements for your primary domain/tenant or Azure subscription:

* **Role** - Any
* **User type** - Member
* **User principal name** - Must have no reference to 'external'
* **Identity** - Must match the tenant’s name for the partnership

<figure><img src="../../../../.gitbook/assets/Untitled design (3).png" alt=""><figcaption><p>Entra ID Users Section</p></figcaption></figure>
