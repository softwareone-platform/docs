# How do I set up SSO?

Our platform has an SSO Authentication framework that integrates with existing Identity provider tools (such as Azure AD and ADFS) and SAML-based tools (such as Okta and Ping).

## Setting up SSO with SAML <a href="#saml" id="saml"></a>

### Process

1. The customer provides SoftwareOne with basic metadata about their IdP. If your SSO tool requires the **Assertion Consumer Service URL** and **Entity ID**, please contact SoftwareOne.
2. SoftwareOne proceeds with a basic setup on the Client Portal IdP and provides you with `{connection_name}` to use for further configuration.
3. You finalize the setup on your side.
4. All logins to the Client Portal for any of the specified IdP domains will be federated out to your SAML-based IdP.

### Information required by the Client Portal

* **IdP Domains** - List of email domains, for example `@user.org`, for which authentication should be federated out to the customer's IdP.
* **Sign In URL** - HTTP-POST or HTTP-Redirect binding.
* **Sign out URL**
* **X509 Signing Certificate**: In the `.pem` or `.cer` format.

### Technical specification

#### Capabilities

We support the items listed in the following table:

<table data-full-width="false"><thead><tr><th>Item</th><th>Details</th></tr></thead><tbody><tr><td>Supported Protocol Bindings</td><td>HTTP-POST &#x26; HTTP-Redirect</td></tr><tr><td>SAML Authentication Requests signed</td><td>Yes (by default)</td></tr><tr><td>Sign Request Algorithm</td><td>RSA-SHA256 (default) or RSA-SHA1</td></tr><tr><td>Sign Request Algorithm Digest</td><td>SHA256 (default) or SHA1</td></tr><tr><td>Signing Certificate Strength</td><td>2048 Bit RSA</td></tr><tr><td>IdP-Initiated SSO</td><td>Supported, but strongly discouraged</td></tr></tbody></table>

#### Settings

The `{connection_name}` is a verbatim string that SoftwareOne will provide after receiving the initial configuration settings from you.

<table data-full-width="false"><thead><tr><th>Setting</th><th>Value</th></tr></thead><tbody><tr><td>Entity ID</td><td><p><code>urn:auth0:pyc:{connection_name}</code>.</p><p><br>Example: If your <code>connection_name</code> is <code>demo_company</code>, the <strong>Entity ID</strong> on Production will be </p><p><code>urn:auth0:pyc:demo_company</code></p></td></tr><tr><td>Assertion Consumer Service URL</td><td><p>https://{idp_base_url}/login/callback?connection={connection_name}</p><p><br>Example: If your <code>connection_name</code> is <code>demo_company</code>, the <strong>Assertion Consumer Service URL</strong> on Production will be:  https://login.pyracloud.com/login/callback?connection=demo_company</p></td></tr><tr><td>Metadata URL</td><td>https://login.pyracloud.com/samlp/metadata?connection={connection_name}</td></tr><tr><td>Single Logout URL</td><td>https://login.pyracloud.com/logout</td></tr><tr><td>Single Login URL</td><td>We strongly discourage using IdP-Initiated SSO flows because they are vulnerable to <a href="https://support.detectify.com/support/solutions/articles/48001048951-login-csrf">Login CSRF attacks</a>. If possible, let the Client Portal initiate the sign-in (and federate out) when required.</td></tr></tbody></table>

#### Attribute mappings

The Client Portal requires the following attributes via the specified mappings:

| Attribute     | Mapping                                                                                                                                                                                                                                                                                      |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `user_id`     | <p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier</p><p></p><p><strong>Fallback URL 1:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn</p><p></p><p><strong>Fallback URL 2:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p> |
| `name`        | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name                                                                                                                                                                                                                                   |
| `email`       | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress                                                                                                                                                                                                                           |
| `given_name`  | <p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname</p><p></p><p><strong>Fallback URL:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p>                                                                                                                |
| `family_name` | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname                                                                                                                                                                                                                                |

The attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, please provide a list of claims to be used for all attributes above.

Please make sure to provide the attribute values as they are without any modifications.\
URLs are sometimes changed by security software, for example, Proofpoint’s Targeted Attack Protection adds `urldefense.com` at the beginning of links.

## Setting up SSO with Azure AD <a href="#azure-a-d" id="azure-a-d"></a>

To set up SSO with the Client Portal via Azure AD, you must complete the following steps. SoftwareOne will then enable SSO with your Azure AD.

### Process

{% stepper %}
{% step %}
#### Register the Client Portal with Azure AD

1. Sign in to the [Microsoft Azure Portal](https://portal.azure.com/). If you have access to more than one tenant, select your account from the upper right. Set your portal session to the Azure AD tenant that you want.
2. Search for and select **Azure Active Directory**.&#x20;
3. Under **Manage**, select **App registrations**.
4. Select **New Registration**.
5. In **Register an application**, enter a meaningful application name to display to the users, for example, Client Portal.
6. In **Supported account types**, select **Accounts in any organizational directory (Any Microsoft Entra directory - Multitenant)**.
7. In **Redirect URI**, select the Redirect URI type as **Web**, and enter your callback URL: https://login.pyracloud.com/login/callback.
8. Click **Register**.
{% endstep %}

{% step %}
#### Create a client secret

SoftwareOne will use the client secret to interact with your Azure subscription on behalf of the created application. Follow these steps to create a secret:

1. From the **Overview** page of the app, select **Certificates & secrets** > **Client secrets** > **New client secret**.
2. Add a description for your client secret.
3. Set the expiration date for the secret.
4. Select **Add**.
5. Make a note of the client's secret value. The value won't be accessible again after you leave this page.



{% hint style="info" %}
We recommend that you create a reminder to renew your client secret at least two weeks before it expires. Once you've created a new secret, provide the value to SoftwareOne so that it can be updated in the system. If your client secret has expired or is no longer valid, you won't be able to sign in to the Client Portal using SSO.
{% endhint %}
{% endstep %}

{% step %}
#### Add API permissions

Follow these steps to add permissions that allow read access to users and the user directory:

1. From the app Overview page, select **API permissions**.&#x20;
2. Under **Configured permissions**, select **Add a permission**.&#x20;
3. Configure permissions for the Microsoft Graph API.
4. After selecting the API, the **Request API Permissions** page is displayed.&#x20;
5. Enable the following permissions:&#x20;
   * Users > User.Read
   * Directory > Directory.Read.All
6. Select **Add permissions** to complete the process.

{% hint style="info" %}
Enabling the **Directory** > **Directory.Read.All** permission is optional. If you want to benefit from future user auto-provisioning, turn it on. However, for SSO to work, this permission is not required.
{% endhint %}
{% endstep %}

{% step %}
#### Send the details to Marketplace Platform support

Gather the following details and send them by email to [marketplace-support@softwareone.com](mailto:marketplace-support@softwareone.com):

| Inputs required           | Notes                                                                                                                                                                                                                                                                      |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Application Client ID     | You can find the Application (client) ID on the overview page of the application created in [Step 1: Register the Client Portal with Azure AD](https://docs.platform.softwareone.com/help-and-support/faqs/how-do-i-set-up-sso#register-the-client-portal-with-azure-a-d). |
| Application Client Secret | Your client secret as created in [Step 2: Create a client secret](https://docs.platform.softwareone.com/help-and-support/faqs/how-do-i-set-up-sso#create-a-client-secret).                                                                                                 |
| Microsoft Azure AD Domain | Your Azure AD domain name. You can find this on your Azure AD directory's overview page in the Microsoft Azure portal.                                                                                                                                                     |
| IdP Domains               | <p>A list of all email domains that must be authenticated through the federated Azure AD, for example, <code>@customer.com</code>. </p><p>Usually 1 domain but can also be multiple.</p>                                                                                   |

After we receive the information, we will finalize the setup. The Client Portal will then automatically start redirecting all users from the specified IdP domains to your Azure AD for federated authentication.
{% endstep %}
{% endstepper %}

### Technical specification

#### Capabilities

We support the items listed in the following table:

<table><thead><tr><th width="284">Item</th><th>Detail</th></tr></thead><tbody><tr><td>Identity API</td><td>Azure Active Directory (v1) (default) &#x26; Microsoft Identity Platform (v2).</td></tr><tr><td>Protocol used for federated Sign-In</td><td>OpenID Connect (default) or WS Federation.</td></tr></tbody></table>

#### Settings

<table><thead><tr><th width="281">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Application type</td><td>Multitenant / Web</td></tr><tr><td>Redirect URI</td><td><p>https://{idp_base_url}/login/callback*</p><p><br>The redirect URI on Production will be: </p><p>https://login.pyracloud.com/login/callback</p></td></tr></tbody></table>

#### Attribute mappings

The Client Portal queries the following basic profile attributes from Azure AD:

* upn
* azure\_id
* given\_name
* family\_name
* nickname
* tenantid
* oid
* email
* name

## Setting up SSO with ADFS <a href="#adfs" id="adfs"></a>

### Process

1. You configure your ADFS server according to technical requirements.
2. You provide ADFS Metadata/IdP domains to SoftwareOne.
3. SoftwareOne will complete the ADFS setup.

### Information required by the Client Portal&#x20;

<table><thead><tr><th width="260">Input</th><th>Notes</th></tr></thead><tbody><tr><td>ADFS Metadata Source</td><td>Either the URL or the Federation Metadata file. The URL usually ends in <code>/FederationMetadata/2007-06/FederationMetadata.xml.</code></td></tr><tr><td>IdP Domains</td><td><p>List of all email domains that should be authenticated through the federated ADFS server, for example, <code>@customer.com</code>. </p><p></p><p>Usually 1 domain, but can also be multiple.</p></td></tr></tbody></table>

### Technical specification

#### Capabilities

We support the items listed in the following table:

<table><thead><tr><th width="269">Item</th><th>Detail</th></tr></thead><tbody><tr><td>Federation Metadata Discovery<br>(Automated Certificate Rollover)</td><td>Yes – if ADFS Metadata Source is provided as URL.</td></tr></tbody></table>

#### Settings

<table data-full-width="false"><thead><tr><th width="262">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Realm Identifier</td><td><p><code>urn:auth0:</code><em><code>{environment_name}</code></em><br></p><p>For example, <code>urn:auth0:pyc</code> in Production.</p></td></tr><tr><td>Endpoint</td><td><p>https://{idp_base_url}/login/callback*<br></p><p>The endpoint URL on Production will be:  https://login.pyracloud.com/login/callback</p></td></tr></tbody></table>

#### Attribute mappings

By default, the Client Portal expects the following attributes from ADFS via the specified mappings:

| LDAP Attribute      | Outgoing Claim Type | Namespace                                                            |
| ------------------- | ------------------- | -------------------------------------------------------------------- |
| E-Mail-Addresses    | E-Mail Address      | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress   |
| Display-Name        | Name                | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name           |
| User-Principal-Name | Name ID             | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier |
| Given-Name          | Given Name          | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname      |
| Surname             | Surname             | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname        |

## Setting up SSO with PingFederate <a href="#ping-federate" id="ping-federate"></a>

### Process

1. You provide sign-in certificates/IdP domains to SoftwareOne.
2. SoftwareOne completes the SSO setup.

### Information required by the Client Portal

1. PingFederate Server URL.
2. X509 signing certificate in the `.pem` or `.cer` format.
3. IdP Domains, including a list of all email domains that should be authenticated through the federated ADFS server (for example, `@customer.com`). Usually just one, but can also be multiple.

### Technical specification

#### Attribute mappings

By default, the Client Portal requires the following attributes via the specified mappings:

| Attribute    | Mappings                                                                                                                                                                                                                                                                                     |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| user\_id     | <p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier</p><p></p><p><strong>Fallback URL 1:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn</p><p></p><p><strong>Fallback URL 2:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p> |
| name         | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name                                                                                                                                                                                                                                   |
| email        | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress                                                                                                                                                                                                                           |
| given\_name  | <p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname</p><p></p><p><strong>Fallback URL:</strong></p><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p>                                                                                                          |
| family\_name | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname                                                                                                                                                                                                                                |

The provided attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, please provide a list of claims to be used for all attributes above.

## Handling unknown or new users (Ad Hoc Provisioning)

If an email domain is federated out to the user's identity provider, it's possible that the Client Portal will receive sign-in attempts from users who are not set up as Client Portal users.

In such cases, if authenticated users from a federated connection are not Client Portal users, their login to Client Portal will fail with an error message stating that their account is not set up and they don't have access.
