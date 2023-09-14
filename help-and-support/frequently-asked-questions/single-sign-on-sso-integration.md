---
description: Learn the technical aspects of the SSO integration.
---

# How to setup single sign-on (SSO)

Our platform has an SSO Authentication framework that integrates with existing Identity provider tools like Azure AD, ADFS, and SAML-based tools like Okta and Ping.

***

### SSO with SAML <a href="#saml" id="saml"></a>

#### **Simplified setup process**

1. The customer provides SoftwareOne with basic metadata about their IdP. If your SSO tool requires to know the Assertion Consumer Service URL and Entity ID, please contact SoftwareONE to get this input.
2. SoftwareONE proceeds with basic setup on the PyraCloud IdP and provides the customer with {connection\_name} that will be used for further configuration.
3. The customer proceeds & finalizes the setup on their end.
4. All logins to PyraCloud for any of the specified IdP domains will now be federated out to the user's SAML-based IdP.

**Required information for setup on the PyraCloud side**

* IdP Domains: List of email domains, for example, @user.org, for which authentication should be federated out to the user's IdP.
* Sign In URL: (HTTP-POST or HTTP-Redirect binding)
* Sign Out URL
* X509 Signing Certificate: in `.pem` or `.cer` format

***

### **Technical specifications**

**Capabilities**

We support the following items, for example, we support HTTP-POST and HTTP-Redirect for protocol bindings.

| Item                                | Details                                |
| ----------------------------------- | -------------------------------------- |
| Supported Protocol Bindings         | HTTP-POST & HTTP-Redirect              |
| SAML Authentication Requests signed | Yes (by default)                       |
| Sign Request Algorithm              | RSA-SHA256 (default) or RSA-SHA1       |
| Sign Request Algorithm Digest       | SHA256 (default) or SHA1               |
| Signing Certificate Strength        | 2048 Bit RSA                           |
| IdP-Initiated SSO                   | Supported, but _strongly_ discouraged. |

**Settings**

`{connection_name}` is a verbatim string that will be shared with you once we receive the initial configuration settings from you.

| **Setting**                    | **Value**                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Entity ID                      | <p><code>urn:auth0:pyc:{connection_name}</code><br>e.g. if your <code>connection_name</code> was <code>demo_company</code>, the Entity ID on production would be <code>urn:auth0:pyc:demo_company</code></p>                                                                                                                                                               |
| Assertion Consumer Service URL | <p>https://login.pyracloud.com/login/callback?connection={connection_name}<br>e.g. if your <em>connection_name</em> is demo_company, the assertion consumer service URL on production would be https://login.pyracloud.com/login/callback/connection=demo_company</p>                                                                                                      |
| Metadata URL                   | https://login.pyracloud.com/samlp/metadata?connection={connection\_name}                                                                                                                                                                                                                                                                                                   |
| Single Logout URL              | https://login.pyracloud.com/logout                                                                                                                                                                                                                                                                                                                                         |
| Single Login URL               | We _strongly_ discourage from using IdP-Initiated SSO flows as they are, by design, vulnerable to [Login CSRF attacks](https://support.detectify.com/support/solutions/articles/48001048951-login-csrf) . If possible, users should navigate to PyraCloud (e.g. via https://apps.pyracloud.com/ ) and let PyraCloud initiate the sign-in (and federate out) when required. |

**Attribute Mappings**

By default, PyraCloud will need the following attributes via the specified mappings from you:

* `user_id` via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier
  * (fallback 1) http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn
  * (fallback 2) http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name
* `name` via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name
* email via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress
* `given_name` via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname
  * (fallback 1) http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname
* `family_name` via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname

The provided attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, please provide a list of claims to be used for all attributes above.

Please make sure to provide the attribute values as they are without any modifications!\
URLs are sometimes changed by security software, e.g. Proofpoint’s Targeted Attack Protection adds urldefense.com to the beginning of links.

***

### SSO with Azure AD <a href="#azure-a-d" id="azure-a-d"></a>

**Simplified Setup Process**

1. The user registers PyraCloud as an application inside their Azure subscription.
2. The user creates a client secret for this application that can then be used by SoftwareONE to interact with the user's Azure subscription on behalf of the created application.
3. The user adds permissions to the application that allow read access to users and the user directory.
4. The user forwards client secrets & additional information to SoftwareONE (see table below).
5. SoftwareONE completes the Single Sign-On setup on the PyraCloud side.

**Required Information for Setup on PyraCloud Side**

| **Required Input**        | **Explanation**                                                                                                                                  |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Application Client ID     | Can be found in the Azure Portal on the overview page of the application created in Step 1. The field is called “Application (client) ID”        |
| Application Client Secret | Created in step 2                                                                                                                                |
| Microsoft Azure AD Domain | The customers Azure AD domain name. It can be found on the Azure AD directory’s overview page in the Microsoft Azure portal                      |
| IdP Domains               | List of all email domains that should be authenticated through the federated Azure AD, e.g. @customer.com. Usually one but can also be multiple. |

**Technical Specifications**

**Capabilities**

We support the following for the below-mentioned items, for example, Azure Active Directory and Microsoft Identity Platform for Identity API.

| Item                                | Detail                                                                   |
| ----------------------------------- | ------------------------------------------------------------------------ |
| Identity API Used                   | Azure Active Directory (v1) (default) & Microsoft Identity Platform (v2) |
| Protocol used for federated Sign-In | OpenID Connect (default) or WS Federation                                |

**Settings**

| Setting          | Value                                                                                                                                                                              |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Application type | Multitenant / Web                                                                                                                                                                  |
| Redirect URI     | <p><code>https://</code><em><code>{idp_base_url}</code></em><code>/login/callback</code>*<br>i.e. the redirect URI on production is https://login.pyracloud.com/login/callback</p> |

**Attribute Mappings**

PyraCloud queries basic profile attributes from Azure AD:

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

### SSO with ADFS <a href="#adfs" id="adfs"></a>

#### **Simplified Setup Process**

* The user configures their ADFS server according to technical requirements (see below).
* User provides ADFS Metadata/IdP domains to SoftwareONE
* SoftwareOne will complete ADFS setup.

#### **Required Information for Setup on the PyraCloud Side**

* ADFS Metadata Source: Either an URL (usually ending in …/FederationMetadata/2007-06/FederationMetadata.xml) or a Federation Metadata File
* IdP Domains: List of all email domains that should be authenticated through the federated ADFS server (e.g. @customer.com). (Usually just one, but can also be multiple.)

#### **Technical Specifications**

**Capabilities**

We support the following for the below-mentioned items.

| Item                                                                     | Detail                                            |
| ------------------------------------------------------------------------ | ------------------------------------------------- |
| <p>Federation Metadata Discovery<br>(Automated Certificate Rollover)</p> | Yes – if ADFS Metadata Source is provided as URL. |

**Settings**

| Setting          | Value                                                                                                                                                                              |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Realm Identifier | <p><code>urn:auth0:</code><em><code>{environment_name}</code></em><br>e.g. urn:auth0:pyc on production</p>                                                                         |
| Endpoint         | <p><code>https://</code><em><code>{idp_base_url}</code></em><code>/login/callback</code>*<br>i.e. the endpoint URL on production is https://login.pyracloud.com/login/callback</p> |

**Attribute Mappings**

PyraCloud by default expects the following attributes from ADFS via the specified mappings:

| LDAP Attribute      | Outgoing Claim Type | Namespace                                                            |
| ------------------- | ------------------- | -------------------------------------------------------------------- |
| E-Mail-Addresses    | E-Mail Address      | ttp://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddressm   |
| Display-Name        | Name                | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name           |
| User-Principal-Name | Name ID             | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier |
| Given-Name          | Given Name          | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname      |
| Surname             | Surname             | http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname        |

***

### SSO with PingFederate <a href="#ping-federate" id="ping-federate"></a>

#### **Simplified Setup Process**

1. User provides Signing Certificates/IdP domains to SoftwareONE
2. SoftwareONE will complete the SSO setup.

#### **Required Information for Setup on the PyraCloud Side**

* PingFederate Server URL
* X509 Signing Certificate in `.pem` or `.cer` format
* IdP Domains: List of all email domains that should be authenticated through the federated ADFS server (e.g. @customer.com). (Usually just one, but can also be multiple.)

**Technical Specifications**

**Attribute Mappings**

By default, PyraCloud requires the following attributes via the specified mappings:

* **user\_id** via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier
  * (fallback 1) http://schemas.xmlsoap.org/ws/2005/05/identity/claims/upn
  * (fallback 2) http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name
* **name** via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name
* **email** via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress
* **given\_name** via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname
  * (fallback 1) http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname
* **family\_name** via
  * http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname

The provided attributes must satisfy at least one mapping for all properties above. If your IdP provides values for the required attributes in different claims/namespaces, please provide a list of claims to be used for all attributes above

***

### Things to watch out for <a href="#things-to-watch-out-for" id="things-to-watch-out-for"></a>

**Handling Unknown / New Users (Ad Hoc Provisioning)**

If an email domain is federated out to the user's identity provider, it is possible that PyraCloud will receive sign-in attempts from users who are not set up as PyraCloud users.

In that case, if authenticated users from a federated connection are not PyraCloud users, their login to PyraCloud will fail with an error message stating that their account is not set up and they do not have access.
