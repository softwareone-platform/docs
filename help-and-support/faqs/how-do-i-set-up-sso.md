# How do I set up SSO?

SoftwareOne Marketplace has an SSO Authentication framework that integrates with existing identity provider tools, such as Azure AD and ADFS, and SAML-based tools, such as Okta and Ping. This topic describes how you can set up SSO with these tools.

## Setting up SSO with SAML <a href="#saml" id="saml"></a>

### Process

Setting up SSO with SAML involves the following steps:&#x20;

1. **Provide IdP metadata to SoftwareOne** - Provide SoftwareOne with basic metadata about your IdP. If your SSO tool requires the **Assertion Consumer Service URL** and **Entity ID**, contact SoftwareOne.
2. **SoftwareOne configures the client portal for your connection** - SoftwareOne proceeds with a basic setup on the Client Portal IdP and provides you with `{connection_name}` to use for further configuration.
3. **You complete your IdP configuration** - Finalize the setup on your side.
4. **Federation becomes active** - All logins to the Client Portal for any of the specified IdP domains are federated out to your SAML-based IdP.

### Information required by the Client Portal

To set up SSO with SAML, SoftwareOne requires the following information:

* **IdP Domains** (list of email domains, for example, `@user.org` for which authentication should be federated out to your IdP)
* **Sign In URL** (HTTP-POST or HTTP-Redirect)
* **Sign out URL**
* **X509 Signing Certificate**  (in the `.pem` or `.cer` format)

### Technical specification

#### Capabilities

<table data-full-width="false"><thead><tr><th width="339">Item</th><th>Details</th></tr></thead><tbody><tr><td>Supported Protocol Bindings</td><td>HTTP-POST &#x26; HTTP-Redirect</td></tr><tr><td>SAML Authentication Requests signed</td><td>Yes (by default)</td></tr><tr><td>Sign Request Algorithm</td><td>RSA-SHA256 (default) or RSA-SHA1</td></tr><tr><td>Sign Request Algorithm Digest</td><td>SHA256 (default) or SHA1</td></tr><tr><td>Signing Certificate Strength</td><td>2048 Bit RSA</td></tr><tr><td>IdP-Initiated SSO</td><td>Supported, but strongly discouraged</td></tr></tbody></table>

#### Settings

The `{connection_name}` is a verbatim string that SoftwareOne provides after receiving your initial configuration settings.

<table data-full-width="false"><thead><tr><th width="275">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Entity ID</td><td><p><code>urn:auth0:pyc:{connection_name}</code>.</p><p><br>Example: If your <code>connection_name</code> is <code>demo_company</code>, the <strong>Entity ID</strong> on Production will be </p><p><code>urn:auth0:pyc:demo_company</code></p></td></tr><tr><td>Assertion Consumer Service URL</td><td><p>https://{idp_base_url}/login/callback?connection={connection_name}</p><p><br>Example: If your <code>connection_name</code> is <code>demo_company</code>, the <strong>Assertion Consumer Service URL</strong> on Production will be:  https://login.pyracloud.com/login/callback?connection=demo_company</p></td></tr><tr><td>Metadata URL</td><td>https://login.pyracloud.com/samlp/metadata?connection={connection_name}</td></tr><tr><td>Single Logout URL</td><td>https://login.pyracloud.com/logout</td></tr><tr><td>Single Login URL</td><td>We strongly discourage using IdP-Initiated SSO flows because they are vulnerable to <a href="https://support.detectify.com/support/solutions/articles/48001048951-login-csrf">Login CSRF attacks</a>. If possible, let the Client Portal initiate the sign-in (and federate out) when required.</td></tr></tbody></table>

#### Attribute mappings

The Client Portal requires the following attributes via specified mappings:

<table><thead><tr><th width="167">Attribute</th><th>Mapping </th></tr></thead><tbody><tr><td><code>user_id</code></td><td><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier</p><p></p><p><strong>Fallback URL 1:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn</p><p></p><p><strong>Fallback URL 2:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p></td></tr><tr><td><code>name</code></td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</td></tr><tr><td><code>email</code></td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress</td></tr><tr><td><code>given_name</code></td><td><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname</p><p></p><p><strong>Fallback URL:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p></td></tr><tr><td><code>family_name</code></td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname</td></tr></tbody></table>

The attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, provide a list of claims to be used for all attributes above.

Make sure to provide the attribute values as they are without any modifications. URLs are sometimes changed by security software, for example, Proofpoint’s Targeted Attack Protection adds `urldefense.com` at the beginning of links.

## Setting up SSO with Azure AD <a href="#azure-a-d" id="azure-a-d"></a>

To set up SSO with the Client Portal via Azure AD, you must complete the following steps. Once these steps are completed, SoftwareOne will enable SSO with your Azure AD.

### Process

Setting up SSO with Azure AD involves the following steps:&#x20;

{% stepper %}
{% step %}
**Register the Client Portal with Azure AD**

1. Sign in to the [Microsoft Azure Portal](https://portal.azure.com/). If you have access to more than one tenant, select your account from the upper right. Set your portal session to the Azure AD tenant that you want.
2. Search for and select **Azure Active Directory**.&#x20;
3. Under **Manage**, select **App registrations**.
4. Select **New Registration**.
5. In **Register an application**, enter a meaningful application name to display to the users, for example, Client Portal.
6. In **Supported account types**, select **Accounts in any organizational directory (Any Microsoft Entra directory - Multitenant)**.
7. In **Redirect URI**, select the Redirect URI type as **Web**, and enter your callback URL: https://login.pyracloud.com/login/callback.
8. Select **Register**.
{% endstep %}

{% step %}
**Create a client secret**

SoftwareOne uses the client secret to interact with your Azure subscription on behalf of the created application.&#x20;

To create a secret:

1. From the **Overview** page of the app, select **Certificates & secrets** > **Client secrets** > **New client secret**.
2. Add a description for your client secret.
3. Set the expiration date for the secret.
4. Select **Add**.
5. Make a note of the client's secret value. The value won't be accessible again after you leave this page.

{% hint style="info" %}
We recommend that you create a reminder to renew your client secret at least two weeks before it expires. Once you've created a new secret, provide the value to SoftwareOne so it can be updated in the system. If your client secret has expired or is no longer valid, you cannot sign in to the Client Portal using SSO.
{% endhint %}
{% endstep %}

{% step %}
**Add API permissions**

To add permissions that allow read access to users and the user directory:

1. From the App Overview page, select **API permissions**.&#x20;
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
**Send details to the Marketplace Platform Support**

Gather the following details and send them to [marketplace-support@softwareone.com](mailto:marketplace-support@softwareone.com):

{% hint style="warning" %}
Any sensitive information, such as SSO secrets or credentials, must be shared in encrypted form. Do not send sensitive data in plain text.&#x20;

If you need help encrypting or securely sharing this information, [contact Marketplace Platform Support](../contact-support.md) before sending the data. Our team can guide you through secure sharing options.
{% endhint %}

<table><thead><tr><th width="261.5">Details</th><th>Notes</th></tr></thead><tbody><tr><td>Application Client ID</td><td>You can find the Application (client) ID on the overview page of the application created in <a href="https://docs.platform.softwareone.com/help-and-support/faqs/how-do-i-set-up-sso#register-the-client-portal-with-azure-a-d">Step 1: Register the Client Portal with Azure AD</a>.</td></tr><tr><td>Application Client Secret</td><td>Your client secret as created in <a href="https://docs.platform.softwareone.com/help-and-support/faqs/how-do-i-set-up-sso#create-a-client-secret">Step 2: Create a client secret</a>.</td></tr><tr><td>Microsoft Azure AD Domain</td><td>Your Azure AD domain name. You can find this on your Azure AD directory's overview page in the Microsoft Azure portal.</td></tr><tr><td>IdP Domains</td><td>A list of all email domains that must be authenticated through the federated Azure AD, for example, <code>@customer.com</code>. Usually 1 domain, but can also be multiple.</td></tr></tbody></table>

After we receive the information, we will finalize the setup. Once the setup is completed, the Client Portal automatically starts redirecting all users from the specified IdP domains to your Azure AD for federated authentication.
{% endstep %}
{% endstepper %}

### Technical specification

#### Capabilities

<table><thead><tr><th width="298">Item</th><th>Detail</th></tr></thead><tbody><tr><td>Identity API</td><td>Azure Active Directory (v1) (default) &#x26; Microsoft Identity Platform (v2).</td></tr><tr><td>Protocol used for federated Sign-In</td><td>OpenID Connect (default) or WS Federation.</td></tr></tbody></table>

#### Settings

<table><thead><tr><th width="289">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Application type</td><td>Multitenant / Web</td></tr><tr><td>Redirect URI</td><td><p>https://{idp_base_url}/login/callback*</p><p><br>The redirect URI on Production will be: </p><p>https://login.pyracloud.com/login/callback</p></td></tr></tbody></table>

#### Attribute mappings

The Client Portal queries the following basic profile attributes from Azure AD:

* `upn`
* `azure_id`
* `given_name`
* `family_name`
* `nickname`
* `tenantid`
* `oid`
* `email`
* `name`

## Setting up SSO with ADFS <a href="#adfs" id="adfs"></a>

### Process

Setting up SSO with ADFS involves the following steps:&#x20;

1. Configure your ADFS server according to technical requirements.
2. Provide ADFS metadata and IdP domains to SoftwareOne.
3. SoftwareOne completes the ADFS setup.

### Information required by the Client Portal

To set up SSO with ADFS, SoftwareOne requires the following information:

* ADFS Metadata Source (either the URL or the Federation Metadata file. The URL usually ends in `/FederationMetadata/2007-06/FederationMetadata.xml` )
* IdP Domains (list of all email domains that must be authenticated through the federated ADFS server, for example, `@customer.com`. Usually 1 domain, but can also be multiple.)

### Technical specification

#### Capabilities

<table><thead><tr><th width="269">Item</th><th>Detail</th></tr></thead><tbody><tr><td>Federation Metadata Discovery<br>(Automated Certificate Rollover)</td><td>Yes – if ADFS Metadata Source is provided as URL.</td></tr></tbody></table>

#### Settings

<table data-full-width="false"><thead><tr><th width="170">Setting</th><th>Value</th></tr></thead><tbody><tr><td>Realm Identifier</td><td><p><code>urn:auth0:</code><em><code>{environment_name}</code></em><br></p><p>For example, <code>urn:auth0:pyc</code> in Production.</p></td></tr><tr><td>Endpoint</td><td><p>https://{idp_base_url}/login/callback*<br></p><p>The endpoint URL in Production will be:  <code>https://login.pyracloud.com/login/callback</code></p></td></tr></tbody></table>

#### Attribute mappings

By default, the Client Portal expects the following attributes from ADFS via the specified mappings:

<table><thead><tr><th width="185">LDAP Attribute</th><th width="191.33333333333331">Outgoing Claim Type</th><th>Namespace</th></tr></thead><tbody><tr><td><code>E-Mail-Addresses</code></td><td>E-Mail Address</td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress</td></tr><tr><td><code>Display-Name</code></td><td>Name</td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</td></tr><tr><td><code>User-Principal-Name</code></td><td>Name ID</td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier</td></tr><tr><td><code>Given-Name</code></td><td>Given Name</td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname</td></tr><tr><td><code>Surname</code></td><td>Surname</td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname</td></tr></tbody></table>

## Setting up SSO with PingFederate <a href="#ping-federate" id="ping-federate"></a>

### Process

Setting up SSO with PingFederate involves the following steps:&#x20;

1. Provide sign-in certificates/IdP domains to SoftwareOne.
2. SoftwareOne completes the SSO setup.

### Information required by the Client Portal

To set up SSO with PingFederate, SoftwareOne requires the following information:

* PingFederate Server URL.
* X509 signing certificate in the `.pem` or `.cer` format.
* IdP Domains, including a list of all email domains that should be authenticated through the federated ADFS server (for example, `@customer.com`). Usually just one, but can also be multiple.

### Technical specification

#### Attribute mappings

By default, the Client Portal requires the following attributes via the specified mappings:

<table><thead><tr><th width="155">Attribute </th><th>Mappings</th></tr></thead><tbody><tr><td><code>user_id</code></td><td><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier</p><p></p><p><strong>Fallback URL 1:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn</p><p></p><p><strong>Fallback URL 2:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p></td></tr><tr><td><code>name</code></td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</td></tr><tr><td><code>email</code></td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress</td></tr><tr><td><code>given_name</code></td><td><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname</p><p></p><p><strong>Fallback URL:</strong></p><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p></td></tr><tr><td><code>family_name</code></td><td>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname</td></tr></tbody></table>

The provided attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, you can provide a list of claims to be used for all attributes above.

## Handling unknown or new users (ad hoc provisioning)

If an email domain is federated out to the user's identity provider, the Client Portal receives sign-in attempts from users who are not set up as Client Portal users.

In such cases, if authenticated users from a federated connection are not Client Portal users, their login to Client Portal will fail with an error message stating that their account is not set up and they don't have access.
