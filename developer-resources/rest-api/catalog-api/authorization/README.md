# Authorization

An Authorization object is a business object that encapsulates the permissions and credentials necessary for interactions between a specific seller and vendors, all within the scope of a single product. It is associated with the seller via listings and serves as the repository for access control and provisioning data required for the vendor to deliver services or content.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="153">Field</th><th width="146">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The identifier for the authorization. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the authorization. </td></tr><tr><td><code>externalIds</code></td><td>object, core</td><td>A reference to the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>eligibility</code></td><td>boolean, core</td><td>Indicates if authorization is enabled for the tier 1 program.</td></tr><tr><td><code>journal</code></td><td>object, core</td><td>Indicates if authorization is enabled for tier 2 program.</td></tr><tr><td><code>currency</code></td><td>string, core</td><td>The currency of the authorization.</td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) Notes for the authorization.</td></tr><tr><td><code>product</code></td><td>object</td><td>(Read-only) The <a href="../product/"><code>product</code></a> that the authorization belongs to. </td></tr><tr><td><code>vendor</code></td><td>object</td><td>(Read-only) The vendor <a href="../../accounts-api/account/">account</a> to which the authorization belongs.</td></tr><tr><td><code>owner</code></td><td>object</td><td>(Read-only) Represents the SoftwareOne <a href="../../accounts-api/seller/"><code>seller</code></a> entity. </td></tr><tr><td><code>statistics</code></td><td>object</td><td>(Read-only) Shows statistics related to the authorization. </td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr><tr><td><code>settings</code></td><td>string</td><td>(Optional) The settings value validated as JSON.</td></tr></tbody></table>

## Authorization Statistics object

<table><thead><tr><th width="151">Field</th><th width="138">Type</th><th>Description</th></tr></thead><tbody><tr><td>subscriptions</td><td>integer</td><td>(Read-only) Number of subscriptions assigned to the Authorization.</td></tr><tr><td>agreements</td><td>integer</td><td>(Read-only) Number of agreements assigned to the Authorization.</td></tr><tr><td>listings</td><td>integer</td><td>(Read-only) Number of listings referring to the Authorization.</td></tr><tr><td>sellers</td><td>integer</td><td>(Read-only) Number of sellers referring to the Authorization.</td></tr></tbody></table>

## Authorization Journal object

<table><thead><tr><th width="152">Field</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>firstInvoiceDate</td><td>datetime</td><td>First invoice data for data submitted by the vendor</td></tr><tr><td>frequency</td><td>string</td><td>The frequency at which the vendor will submit journal data.</td></tr></tbody></table>

## Authorization Eligibility object

<table><thead><tr><th width="147">Field</th><th width="135">Type</th><th>Description</th></tr></thead><tbody><tr><td>client</td><td>boolean</td><td>Indicates direct client</td></tr><tr><td>partner</td><td>boolean</td><td>Indicates indirect client, also called partners.</td></tr></tbody></table>

## Example

{% code title="AUTHORIZATION OBJECT" overflow="wrap" lineNumbers="true" %}
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
  "journal": {
    "firstInvoiceDate": "2023-12-14T17:28:57Z",
    "frequency": "Monthly"
  },
  "eligibility": {
    "client": true,
    "partner": true
  },
  "statistics": {
      "subscriptions": 5,
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
