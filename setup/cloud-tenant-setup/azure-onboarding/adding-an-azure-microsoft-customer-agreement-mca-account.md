---
description: Follow this topic to add your Azure MCA account to the Client Portal.
---

# Adding an Azure Microsoft Customer Agreement (MCA) Account

***

The Client Portal supports both legacy EA and modern [MCA ](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/mca-overview)models.&#x20;

Before proceeding further, make sure that you've followed the steps in [Activating your account](adding-an-azure-enterprise-agreement-ea-account.md#activating-your-account).

### Prerequisites <a href="#how-to-onboard-mca-tenant" id="how-to-onboard-mca-tenant"></a>

Ensure that your account has the proper billing account type set up. To verify:&#x20;

1. Sign in to the [Azure Portal](https://portal.azure.com).
2. From the left navigation pane, select **Cost Management + Billing.**
3. Navigate to **Settings** > **Properties** to verify your Azure billing account type.

<figure><img src="../../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

### Assigning the Billing Account Reader role (Azure Portal)

**To assign the Billing account reader role to the Client Portal**

1. Sign in to the [Azure Portal](https://portal.azure.com). Search for **Cost Management + Billing.**
2. In the left navigation pane, select **Billing scopes** and then select your MCA billing scope.

<figure><img src="../../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

3. Select **Access Control (IAM)** to assign permissions.&#x20;

<figure><img src="../../../.gitbook/assets/image (13) (1).png" alt=""><figcaption></figcaption></figure>

4. Select **Add** and then from the Role dropdown list, select **Billing account reader**.

<figure><img src="../../../.gitbook/assets/image (14) (1).png" alt=""><figcaption></figcaption></figure>

5. Select the **PyraCloud (Azure)** application. &#x20;

![](<../../../.gitbook/assets/image (18).png>)

6. Select **Save**.&#x20;

Your MCA billing data will be synchronized with the Client Portal after 24 hours.
