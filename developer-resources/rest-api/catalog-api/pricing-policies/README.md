# Pricing Policy

The Pricing Policy object contains the following attributes:

<table data-search="false"><thead><tr><th width="134">Field</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The identifier of the pricing policy.</td></tr><tr><td><code>client</code></td><td>object, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The client <a href="../../accounts-api/account/"><code>account</code></a> to which the pricing policy belongs.</td></tr><tr><td><code>markup</code></td><td>decimal</td><td>The markup that has been applied to the yield cap. Optional on request: if omitted, the markup requires a margin to be provided. Only SoftwareOne operations can view this field. </td></tr><tr><td><code>margin</code></td><td>decimal</td><td>The margin of the yield cap. Optional on request: if omitted, the markup requires a margin to be provided. Only SoftwareOne operations can view this field. </td></tr><tr><td><code>products</code></td><td>object, core</td><td><p>Represents the <a href="../product/"><code>product</code></a> object, containing a list of selected products. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "PRD-1111-1111-1111",    
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  }
]
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td><p>Indicates the status of the price policy. Allowed values are:</p><ul><li><code>Active</code></li><li><code>Disabled</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>eligibility</code></td><td>decimal</td><td><p>Indicates whether the policy applies to clients (Tier 1), partners (Tier 2), or both. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  "client": true,
  "partner": false
]
</code></pre></td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the pricing policy.</td></tr><tr><td><code>externalIds</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>notes</code></td><td>string</td><td>User notes about the pricing policy.</td></tr><tr><td><code>statistics</code></td><td>object</td><td>Represents the <a href="./#pricingpolicystatistics-object"><code>pricingPolicyStatistics</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Pricing Policy Attachment object <a href="#pricingpolicyattachment-object" id="pricingpolicyattachment-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="178">Field</th><th width="173">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The ID of the attachment. </td></tr><tr><td><code>name</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>The name of the attachment. </td></tr><tr><td><code>type</code></td><td>string</td><td>The type of file.</td></tr><tr><td><code>size</code></td><td>integer</td><td>The size of the file.</td></tr><tr><td><code>description</code></td><td>string, core</td><td>A description of the attachment. </td></tr><tr><td><code>fileName</code></td><td>string</td><td>The name of the file.</td></tr><tr><td><code>contentType</code></td><td>string</td><td>Indicates the content type. </td></tr><tr><td><code>status</code></td><td>enum, core</td><td>Indicates the status of the pricing policy attachment.</td></tr><tr><td><code>audit</code></td><td>object</td><td>Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Pricing Policy Statistics object <a href="#pricingpolicystatistics-object" id="pricingpolicystatistics-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="168">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>orders</code></td><td>number</td><td>The number of orders assigned to the policy. </td></tr><tr><td><code>attachments</code></td><td>number</td><td>The number of attachments assigned to the policy.</td></tr></tbody></table>

## Eligibility object <a href="#eligibility" id="eligibility"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="163">Field</th><th width="140">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>client</code></td><td>boolean</td><td>Indicates direct clients. </td></tr><tr><td><code>partner</code></td><td>boolean</td><td>Indicates indirect clients, also called partner.</td></tr></tbody></table>

## Example

{% code title="PRICING POLICY OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "PRP-1234-1222-5678",   
    "client": {
        "id": "ACC-1234-1222",        
        "name": "Microsoft",
        "icon": "/static/ACC-1234-1222/account.png"
    },
    "markup": "0.5013",
    "margin": "0.3339",
    "products": [
      {
        "id": "PRD-1111-1111-1111",        
        "name": "Microsoft Office 365 NCE",
        "icon": "/static/PRD-1111-1111-1111/logo.png"
      }
    ],
    "status": "Active",
    "name": "PRP for Stark Industries",
    "externalIds": {
        "operations": "op-322-322"
    },
    "notes": "This is the primary Pricing Policy for the EU region",
    "statistics": {
        "orders": 2,
        "attachments": 1
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
