# Authorizations

An authorization object is a business object that encapsulates the permissions and credentials necessary for interactions between a specific seller and vendors, all within the scope of a single product. It is associated with the seller via listings and serves as the repository for access control and provisioning data required for the vendor to deliver services or content.

The Authorization object contains the following attributes:

<table><thead><tr><th width="126">Field</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier for the authorization. </p><p>Example: AUT-1234-4678</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the authorization. </p><p>Example: Salesforce Enterprise License</p></td></tr><tr><td>externalIds</td><td><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>eligibility</td><td><code>boolean</code></td><td>Indicates if authorization is enabled for the tier 1 program</td></tr><tr><td>tier2</td><td><code>boolean</code></td><td>Indicates if authorization is enabled for tier 2 program</td></tr><tr><td>currency</td><td><code>string</code></td><td>Authorization currency.</td></tr><tr><td>notes</td><td><code>string</code></td><td>Optional notes for the authorization.</td></tr><tr><td>product</td><td><a href="../product/"><code>product</code></a></td><td><p>The product that the authorization belongs to. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{    
  "id": "PRD-1111-1111",  
  "name": "Microsoft Office 365 NCE",
  "icon": "/static/PRD-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>The vendor to which the authorization belongs. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "ACC-1234-1234",  
  "name": "Microsoft",
  "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>owner</td><td><a href="../../accounts-api/seller/"><code>seller</code></a></td><td><p>The SoftwareOne seller entity. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "SEL-1234-4567", 
  "name": "SoftwareOne, Inc."
}
</code></pre></td></tr><tr><td>statistics</td><td><code>authorizationstatistics</code></td><td><p>The statistics related to the authorization. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "subscriptions": 5,
  "agreements": 10,
  "listings": 3,
  "sellers": 2
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "created": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": { ... }
  },
  "updated": { 
    "at": "2023-12-14T17:28:57Z", 
    "by": { ... }
  }
}
</code></pre></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="AUTHORIZATION OBJECT" %}
{% code lineNumbers="true" %}
```json
{
  "id": "AUT-1234-4678",
  "name": "Salesforce Enterprise License",
  "externalId": "WW-1001111",
  "currency": "EUR",
  "notes": "Notes about given authorization",
  "partnerProgram": true,
  "tier1": true,
  "tier2": false,
  "product": {
      "id": "PRD-1111-1111",    
      "name": "Microsoft Office 365 NCE",
      "icon": "/static/PRD-1111-1111/logo.png"
  },
  "vendor": {
    "id": "ACC-1234-1234",  
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
  },
  "owner": {
      "id": "SEL-1234-4567",        
      "name": "SoftwareOne, Inc."
  },
  "statistics": {
      "subscriptions" : 5,
      "agreements": 10,
      "listings": 4,
      "sellers": 1
  },
  "audit": {
    "created": { 
      "at": "2023-12-14T17:28:57Z", 
      "by": {
        "id": "UR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      }
    },
    "updated": { 
      "at": "2023-12-14T17:28:57Z", 
      "by": {
        "id": "UR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/UR-1234-1234-1234.icon.svg"
      }
    }
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
