# GDAP and Partner Relationship Request Considerations

This topic describes some of the key points to keep in mind when establishing a GDAP or a partner relationship request with SoftwareOne.&#x20;

## Primary domain or tenant ID

To establish a  GDAP admin relationship, make sure that your primary domain name or tenant ID in the purchase order matches the details in the Microsoft 365 Admin Center or Microsoft Azure Management Portal.&#x20;

There are a few ways to verify your domain name and ID:

* **Through the Marketplace Platform** - Navigate to the **Parameters** tab on the order details page.
  * The domain name for existing cloud accounts is displayed in the **Existing domain name** field. For new cloud accounts, the **Primary domain name** field shows the domain name.&#x20;
  * The tenant ID is displayed in the **Fulfillment** section.

<figure><img src="../../../.gitbook/assets/csp_parameters.jpg" alt=""><figcaption><p>Parameters tab</p></figcaption></figure>

* **Through Microsoft 365 Admin Center** - Sign in to [Microsoft Entra admin center](https://entra.microsoft.com/) and navigate to **Settings** > **Domains**. Your domain name is displayed on the Domains page.&#x20;

<figure><img src="../../../.gitbook/assets/csp_settings_domain.png" alt=""><figcaption><p>Microsoft 365 admin center</p></figcaption></figure>

* **Through the Azure Portal** - Sign in to the [Azure portal](https://portal.azure.com/) and navigate to **Entra ID** > **Overview**. Your registered primary domain is displayed in the **Name** section.

<figure><img src="../../../.gitbook/assets/csp_entra_ID.png" alt=""><figcaption><p>Azure entra ID overview</p></figcaption></figure>

## Regional market restrictions

To establish a successful partner and GDAP admin relationship, both SoftwareOne and your organization must operate within the same Microsoft-defined regional market.&#x20;

For instance, SoftwareOne Brazil can only transact with customers in Brazil. For details on the CSP regions and markets, see the [Region availability](https://learn.microsoft.com/en-us/partner-center/enroll/regional-authorization-overview#africa-region-and-market) section in Microsoft's documentation.

The SoftwareOne region applicable to your order is also listed in your purchase order in the Marketplace Platform. To verify, open the details page of your order and select the **Details** tab. The **References** section displays the region.

<figure><img src="../../../.gitbook/assets/csp_authorization.png" alt=""><figcaption><p>Details tab on the order details page</p></figcaption></figure>

You can also verify your organization's region in the Microsoft 365 Admin Center. To do this, sign in to the admin center and navigate to **Settings** > **Org Settings** > **Organization Information**. The name is displayed in the **Country or region** field.

<figure><img src="../../../.gitbook/assets/csp_organization_information.png" alt=""><figcaption><p>Organization information in Microsoft 365 Admin Center</p></figcaption></figure>

## Global administrator role requirements

The user setting up the partner and GDAP admin relationship must meet the following requirements for their primary domain or tenant:

* **Role** - Global Administrator
* **User type** - Member
* **User principal name** - Must have no reference to 'external'
* **Identity** - Must match the tenant’s name for the partnership

<figure><img src="../../../.gitbook/assets/csp_users.png" alt=""><figcaption><p>Users section in Microsoft Entra ID</p></figcaption></figure>
