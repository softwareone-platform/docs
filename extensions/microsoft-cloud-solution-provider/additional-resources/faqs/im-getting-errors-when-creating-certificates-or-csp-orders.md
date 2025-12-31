# I'm getting errors when creating certificates or CSP orders

If you encounter an error during the certificate creation process or when submitting an order, use these steps to validate your partner information in Microsoft Partner Center before retrying certificate creation or CSP orders.

### Verify that the PLA ID (formerly MPN ID) is valid

A Partner Location Account (PLA) ID represents a specific partner location and is required for CSP transactions. Only a PLA ID can be used for CSP orders.&#x20;

Therefore, it's important to verify that this ID is both correct and valid. You can check the ID in the **Identifiers** section of Partner Center.

To verify the PLA ID:

1. Sign in to [Partner Center](https://partner.microsoft.com/dashboard/home) using your global admin credentials.
2. Select the **Settings** (gear) icon.
3. Choose **Account settings**, and then select **Identifiers** under **Organization Profile**.
4. Under **Microsoft AI Cloud Partner Program**, review the list of partner locations and confirm the following:
   1. The **Partner ID** is associated with a `PartnerLocation`.
   2. The location matches the country or region where the CSP order is placed.

Once verified, ensure that the same ID appears in the Marketplace Platform. To verify:

1. Open the Marketplace order and select the **Certificates** tab.
2. Select the certificate, then select the **Parameters** tab.
3. Under **Ordering** parameters, check the **Microsoft Partner Network ID**. The ID must match the PLA ID in Partner Center. If it doesn’t, contact [Marketplace Platform Support](../../../../help-and-support/contact-support.md).

### Confirm that the MPA has been accepted

Microsoft requires an active and signed Microsoft Partner Agreement (MPA) for Partner of Record (POR) validation. You can check whether you have accepted the MPA in the **Agreements** section of Partner Center.

To verify that the MPA is accepted:

1. Sign in to [Partner Center](https://partner.microsoft.com/dashboard/home) using your global admin credentials.
2. Select the **Settings** (gear) icon.
3. Choose **Account settings**, then select **Agreements**.
4. Confirm that **Microsoft Partner Agreement** is listed in the table and that you have accepted it. Additionally, verify that there are no pending actions.

{% hint style="danger" %}
If the agreement isn’t signed or has expired, CSP orders are blocked in the Marketplace Platform.
{% endhint %}

### Verify that the reseller tenant is active

The reseller tenant linked to the PLA ID must be authorized and active. You can check this in the **Legal Info** section of Partner Center.

To verify that the reseller tenant is active:

1. Sign in to [Partner Center](https://partner.microsoft.com/dashboard/home) using your global admin credentials.
2. Select the **Settings** (gear) icon.
3. Choose **Account settings**, and then select **Legal Info** under **Organization Profile**.
4. Confirm the following:
   * The **Verification status** is marked as **Authorized**.
   * The **Microsoft AI Cloud Partner Program** **status** is shown as **Active**.
   * There are no suspensions, deactivations, or compliance holds in place.

If the status is incorrect, contact [Microsoft Partner Support](https://learn.microsoft.com/en-us/partner-center/support/report-problems-with-partner-center).

### Confirm that the PLA region matches the CSP order region

Ensure that the PLA region matches the CSP order region. For example, if a CSP order is placed in France, the PLA must correspond to a Partner Location in France.&#x20;

Using a PLA from a different region (for example, Germany or the United States) results in an error.

### Additional resources

For further information on common errors and troubleshooting tips, see [Partner with Distributors in the Cloud Solution Provider (CSP) Program](https://learn.microsoft.com/en-us/partner-center/customers/indirect-provider-tasks-in-partner-center#common-error-messages-and-how-to-fix-them) in the Microsoft Partner Center documentation.
