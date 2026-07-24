# Microsoft Customer Agreement (MCA)

The Microsoft Customer Agreement (MCA) is Microsoft's contract for purchasing and using cloud services. It defines the terms and conditions that govern Microsoft cloud subscriptions and services.

Before Microsoft cloud services can be provisioned, customers must review and accept the MCA.

### MCA acceptance requirements

Customers purchasing Microsoft cloud services through the Cloud Solution Provider (CSP) program must accept the MCA before subscriptions or services can be provisioned. &#x20;

This requirement applies to:

* Organizations purchasing Microsoft cloud services, such as Azure, Microsoft 365, Dynamics 365, and more for the first time through a CSP partner must also accept the MCA.
* Existing CSP customers who haven't previously accepted the MCA must also accept it.&#x20;
* Customers whose CSP partner accepted the MCA on their behalf before 1 April 2023, and who are required to reaccept the agreement under Microsoft's updated requirements.

### MCA validation in Marketplace Platform

To comply with Microsoft's requirements, Marketplace Platform automatically checks whether the MCA has been accepted when processing orders.

* If the MCA has been accepted, order processing continues.
* If acceptance is required, the order enters a **Querying** status, and processing is paused until the MCA is reviewed and accepted.

### Review and accept the MCA

To review and accept the MCA:

1. Sign in to the [Microsoft 365 Admin Center](https://admin.microsoft.com/AdminPortal/Home?ref=/BillingAccounts/agreement) using your Global Administrator credentials.
2. Navigate to **Billing** or **Account**.
3. Read the terms and conditions of the agreement.
4. Select the checkbox to confirm that you have read and accept the terms and conditions.
5. Select **Accept**.&#x20;

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption><p>Accept the Microsoft Customer Agreement in the Microsoft 365 Admin Center.</p></figcaption></figure></div>

After you accept the MCA and Microsoft confirms your acceptance, your Marketplace order automatically changes from **Querying** to **Processing**.

If the order doesn't automatically change to processing after accepting the MCA, select **Process** on the order details page to update the status manually. For instructions, see [Change status from Querying to Processing](../../../modules-and-features/marketplace/orders/set-an-order-to-processing.md).
