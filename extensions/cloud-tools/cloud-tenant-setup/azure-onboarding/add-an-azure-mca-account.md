---
description: Add your Azure Microsoft Customer Agreement account to the Client Portal.
---

# Add an Azure MCA Account

The Client Portal supports both legacy Enterprise Agreement and modern [Microsoft Customer Agreement](https://learn.microsoft.com/en-us/azure/cost-management-billing/understand/mca-overview) models.  If you are adding an EA or MPSA account, see [Activating an Azure EA or MPSA account](activate-an-azure-ea-or-mpsa-account.md).

## Before you begin <a href="#before-you-start" id="before-you-start"></a>

Before adding an account, note the following points:

* Make sure you've followed the steps in [Activating your account](activate-an-azure-ea-or-mpsa-account.md#activating-your-account).
* Make sure your account has the proper billing account type set up. To verify this, launch the [Azure Portal](https://portal.azure.com). From the left navigation pane, select **Cost Management + Billing**. Then, navigate to **Settings** > **Properties**. The account type is displayed in the right pane.

## Assign the Billing Account Reader role (Azure Portal)

Follow these steps to assign the **Billing account reader** role to the Client Portal:

1. Sign in to the [Azure Portal](https://portal.azure.com) and search for **Cost Management + Billing**.
2. In the left navigation pane, select **Billing scopes** and then select your MCA billing scope.

<div data-full-width="false">

<figure><img src="../../../../.gitbook/assets/image (12) (1) (1) (1) (1) (1) (1).png" alt="" width="482"><figcaption></figcaption></figure>

</div>

3. Select **Access Control (IAM)** to assign permissions.&#x20;

<div data-full-width="false">

<figure><img src="../../../../.gitbook/assets/image (13) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="482"><figcaption></figcaption></figure>

</div>

4. Select **Add** and then from the Role dropdown list, select **Billing account reader**.

<div data-full-width="false">

<figure><img src="../../../../.gitbook/assets/image (14) (1) (1) (1) (1) (1) (1).png" alt="" width="439"><figcaption></figcaption></figure>

</div>

5. Select the **PyraCloud (Azure)** application. &#x20;
6. Select **Save**. Your MCA billing data will be synchronized with the Client Portal after 24 hours.
