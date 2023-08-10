---
description: Add your Azure MCA account to the Client Portal.
---

# Adding Azure Microsoft Customer Agreement (MCA) account

The Client Portal supports both legacy EA and modern [MCA ](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/mca-overview)models. Before reading further please make sure you have followed the steps in [Activating your account](adding-azure-enterprise-agreement-ea-account.md#activating-your-account).

#### To onboard your MCA tenant <a href="#how-to-onboard-mca-tenant" id="how-to-onboard-mca-tenant"></a>

1. Verify that your account has the proper billing account type set up. You can verify this in the [Azure Portal](https://portal.azure.com) > **Cost Management + Billing > Properties.**

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

2. Add the Billing Reader role to the Client Portal. To do so:
   * Sign in to the [Azure Portal](https://portal.azure.com). Search for **Cost Management + Billing.**
   * Select your MCA Billing Scope.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

3. Select **Access Control (IAM)** to assign permissions.&#x20;

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

4. Select **Add** and choose **Billing Account Reader** from the list of roles.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

5. Select **Service Principle** in the select section of the panel.&#x20;
6. Save your changes.&#x20;
