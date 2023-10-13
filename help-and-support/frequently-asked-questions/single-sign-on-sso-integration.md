---
description: Learn the technical aspects of the SSO integration.
---

# How to setup single sign-on (SSO)

Our platform has an SSO Authentication framework that integrates with existing Identity provider tools (such as Azure AD and ADFS) and SAML-based tools (such as Okta and Ping).

***

## Setting up SSO with SAML <a href="#saml" id="saml"></a>

### **Setup process**

1. The customer provides SoftwareOne with basic metadata about their IdP. If your SSO tool requires the **Assertion Consumer Service URL** and **Entity ID**, please contact SoftwareOne.
2. SoftwareOne proceeds with a basic setup on the Client Portal IdP and provides the customer with `{connection_name}` that'll be used for further configuration.
3. The customer proceeds and finalizes the setup from their side.
4. All logins to the Client Portal for any of the specified IdP domains will be federated out to the customer's SAML-based IdP.

### **Setup information required by the Client Portal**

1. **IdP Domains**: List of email domains, for example `@user.org`, for which authentication should be federated out to the customer's IdP.
2. **Sign In URL**: HTTP-POST or HTTP-Redirect binding.
3. **Sign Out URL**
4. **X509 Signing Certificate**: In the `.pem` or `.cer` format.

### **Technical specification**

#### **Capabilities**

We support the items listed in the following table:

<table data-full-width="false"><thead><tr><th>Item</th><th>Details</th></tr></thead><tbody><tr><td>Supported Protocol Bindings</td><td>HTTP-POST &#x26; HTTP-Redirect</td></tr><tr><td>SAML Authentication Requests signed</td><td>Yes (by default)</td></tr><tr><td>Sign Request Algorithm</td><td>RSA-SHA256 (default) or RSA-SHA1</td></tr><tr><td>Sign Request Algorithm Digest</td><td>SHA256 (default) or SHA1</td></tr><tr><td>Signing Certificate Strength</td><td>2048 Bit RSA</td></tr><tr><td>IdP-Initiated SSO</td><td>Supported, but strongly discouraged</td></tr></tbody></table>

#### **Settings**

`{connection_name}` is a verbatim string that SoftwareOne will provide after receiving the initial configuration settings from you.

<table data-full-width="false"><thead><tr><th>Setting</th><th>Value</th></tr></thead><tbody><tr><td>Entity ID</td><td><p><code>urn:auth0:pyc:{connection_name}</code>.</p><p><br>Example: If your <code>connection_name</code> is <code>demo_company</code>, the <strong>Entity ID</strong> on Production will be </p><p><code>urn:auth0:pyc:demo_company</code></p></td></tr><tr><td>Assertion Consumer Service URL</td><td><p>https://{idp_base_url}/login/callback?connection={connection_name}</p><p><br>Example: If your <code>connection_name</code> is <code>demo_company</code>, the <strong>Assertion Consumer Service URL</strong> on Production will be:  https://login.pyracloud.com/login/callback?connection=demo_company</p></td></tr><tr><td>Metadata URL</td><td>https://login.pyracloud.com/samlp/metadata?connection={connection_name}</td></tr><tr><td>Single Logout URL</td><td>https://login.pyracloud.com/logout</td></tr><tr><td>Single Login URL</td><td>We strongly discourage using IdP-Initiated SSO flows because they are vulnerable to <a href="https://support.detectify.com/support/solutions/articles/48001048951-login-csrf">Login CSRF attacks</a>. If possible, let the Client Portal initiate the sign-in (and federate out) when required.</td></tr></tbody></table>

#### **Attribute Mappings**

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

***

## Setting up SSO with Azure AD <a href="#azure-a-d" id="azure-a-d"></a>

### **Setup Process**

1. The customer registers the Client Portal as an application inside their Azure subscription.
2. The customer creates a client secret for this application that can then be used by SoftwareOne to interact with the user's Azure subscription on behalf of the created application.
3. The customer adds permissions to the application that allow read access to users and the user directory.
4. The customer forwards their client secrets and additional information to SoftwareOne.
5. SoftwareOne completes the SSO setup on the Client Portal side.

### **Setup information required by the Client Portal**&#x20;

| Inputs Required           | Notes                                                                                                                                                           |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Application Client ID     | You can find the **Application (client) ID** on the **Overview** page of the application created in Step 1 (in the Azure Portal).                               |
| Application Client Secret | Created in step 2.                                                                                                                                              |
| Microsoft Azure AD Domain | The customer's Azure AD domain name. You can find it on the Azure AD directory’s **Overview** page of the Azure portal.                                         |
| IdP Domains               | A list of all email domains that must be authenticated through the federated Azure AD, for example, `@customer.com`. Usually 1 domain but can also be multiple. |

### **Technical specification**

#### **Capabilities**

We support the items listed in the following table:

| Item                                | Detail                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------- |
| Identity API                        | Azure Active Directory (v1) (default) & Microsoft Identity Platform (v2). |
| Protocol used for federated Sign-In | OpenID Connect (default) or WS Federation.                                |

#### **Settings**

| Setting          | Value                                                                                                                                             |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Application type | Multitenant / Web                                                                                                                                 |
| Redirect URI     | <p>https://{idp_base_url}/login/callback*</p><p><br>The redirect URI on Production will be: </p><p>https://login.pyracloud.com/login/callback</p> |

#### **Attribute Mappings**

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

***

## Setting up SSO with ADFS <a href="#adfs" id="adfs"></a>

### **Setup Process**

1. The customer configures their ADFS server according to technical requirements.
2. The customer provides ADFS Metadata/IdP domains to SoftwareOne.
3. SoftwareOne will complete the ADFS setup.

### **Setup information required by the Client Portal**&#x20;

| Input                | Notes                                                                                                                                                                                               |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ADFS Metadata Source | Either the URL or the Federation Metadata file. The URL usually ends in `/FederationMetadata/2007-06/FederationMetadata.xml.`                                                                       |
| IdP Domains          | <p>List of all email domains that should be authenticated through the federated ADFS server, for example, <code>@customer.com</code>. </p><p></p><p>Usually 1 domain, but can also be multiple.</p> |

### **Technical specification**

#### **Capabilities**

We support the items listed in the following table:

| Item                                                                     | Detail                                            |
| ------------------------------------------------------------------------ | ------------------------------------------------- |
| <p>Federation Metadata Discovery<br>(Automated Certificate Rollover)</p> | Yes – if ADFS Metadata Source is provided as URL. |

#### **Settings**

<table data-full-width="false"><thead><tr><th>Setting</th><th>Value</th></tr></thead><tbody><tr><td>Realm Identifier</td><td><p><code>urn:auth0:</code><em><code>{environment_name}</code></em><br></p><p>For example, <code>urn:auth0:pyc</code> on Production.</p></td></tr><tr><td>Endpoint</td><td><p>https://{idp_base_url}/login/callback*<br></p><p>The endpoint URL on Production will be:  https://login.pyracloud.com/login/callback</p></td></tr></tbody></table>

#### **Attribute Mappings**

By default, the Client Portal expects the following attributes from ADFS via the specified mappings:

| LDAP Attribute      | Outgoing Claim Type | Namespace                                                            |
| ------------------- | ------------------- | -------------------------------------------------------------------- |
| E-Mail-Addresses    | E-Mail Address      | ttp://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress    |
| Display-Name        | Name                | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name           |
| User-Principal-Name | Name ID             | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier |
| Given-Name          | Given Name          | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname      |
| Surname             | Surname             | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname        |

***

## Setting up SSO with PingFederate <a href="#ping-federate" id="ping-federate"></a>

### **Setup Process**

1. The customer provides Signing Certificates/IdP domains to SoftwareOne.
2. SoftwareOne will complete the SSO setup.

### **Setup information required by the Client Portal**

1. PingFederate Server URL.
2. X509 Signing Certificate in the `.pem` or `.cer` format.
3. IdP Domains: List of all email domains that should be authenticated through the federated ADFS server (for example, `@customer.com`). Usually just one, but can also be multiple.

### **Technical specification**

**Attribute Mappings**

By default, the Client Portal requires the following attributes via the specified mappings:

| Attribute    | Mappings                                                                                                                                                                                                                                                                                     |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| user\_id     | <p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier</p><p></p><p><strong>Fallback URL 1:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn</p><p></p><p><strong>Fallback URL 2:</strong> http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p> |
| name         | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name                                                                                                                                                                                                                                   |
| email        | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress                                                                                                                                                                                                                           |
| given\_name  | <p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname</p><p></p><p><strong>Fallback URL:</strong></p><p>http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name</p>                                                                                                          |
| family\_name | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname                                                                                                                                                                                                                                |

The provided attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, please provide a list of claims to be used for all attributes above.

***

## **Handling unknown or new users (Ad Hoc Provisioning)**

If an email domain is federated out to the user's identity provider, it's possible that the Client Portal will receive sign-in attempts from users who are not set up as Client Portal users.

In such cases, if authenticated users from a federated connection are not Client Portal users, their login to Client Portal will fail with an error message stating that their account is not set up and they don't have access.
