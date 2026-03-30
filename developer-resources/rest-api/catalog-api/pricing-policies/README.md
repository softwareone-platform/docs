# Pricing Policy

The Pricing Policy object contains the following attributes:

<table><thead><tr><th width="134">Field Name</th><th width="227">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The identifier of the pricing policy.</td></tr><tr><td><code>client</code></td><td><a href="../../accounts-api/account/">account</a></td><td>The client to whom the pricing policy belongs.</td></tr><tr><td><code>markup</code></td><td>decimal</td><td>The markup that has been applied to the yield cap. Optional on request: if omitted, the markup requires a margin to be provided. Only SoftwareOne operations can view this field. Example: 0.5013</td></tr><tr><td><code>margin</code></td><td>decimal</td><td><p>The margin of the yield cap. Optional on request: if omitted, the markup requires a margin to be provided. Only SoftwareOne operations can view this field. </p><p>Example: 0.3339</p></td></tr><tr><td><code>products</code></td><td><a href="../product/">product</a></td><td><p>Contains a list of selected products. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "PRD-1111-1111-1111",    
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  }
]
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td><p>Indicates the status of the price policy. </p><p>Allowed values: <code>active</code>, <code>disabled</code>, or <code>deleted</code>.</p></td></tr><tr><td><code>eligibility</code></td><td>decimal</td><td><p>Indicates whether the policy applies to clients (Tier 1), partners (Tier 2), or both. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  "client": true,
  "partner": false
]
</code></pre></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the pricing policy.</p><p>Example: PRP for Stark Industries</p></td></tr><tr><td><code>externalIds</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/externalids.md"><code>externalIds</code></a> object.</td></tr><tr><td><code>notes</code></td><td>string</td><td><p>User notes about the pricing policy.</p><p>Example: This is the primary pricing policy for the EU.</p></td></tr><tr><td><code>statistics</code></td><td>object</td><td>A reference to the <a href="./#pricingpolicystatistics-object"><code>pricingPolicyStatistics</code></a> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Pricing Policy Attachment object <a href="#pricingpolicyattachment-object" id="pricingpolicyattachment-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="173">Field Name</th><th width="123">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The ID of the attachment. </p><p>Example: PPA-1234-1222-1234-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the attachment. </p><p>Example: Pricing policy negotiation 2025</p></td></tr><tr><td><code>type</code></td><td>string</td><td><p>The type of file.</p><p>Example: Text</p></td></tr><tr><td><code>size</code></td><td>integer</td><td><p>The size of the file.</p><p>Example: 123</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the attachment. </p><p>Example: This policy outlines the negotiated pricing terms between SoftwareOne and Stark Industries, established in August 2025. It details the specific pricing policies tailored to the needs of both parties.</p></td></tr><tr><td><code>fileName</code></td><td>string</td><td><p>The name of the file.</p><p>Example: 01984827423.pdf</p></td></tr><tr><td><code>contentType</code></td><td>string</td><td><p>Indicates the content type. </p><p>Example: application/x-pdf</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>Indicates the status of the pricing policy attachment. Example: Active</td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## PricingPolicyStatistics object <a href="#pricingpolicystatistics-object" id="pricingpolicystatistics-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="168">Field Name</th><th width="134">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>orders</code></td><td>number</td><td><p>The number of orders assigned to the policy. </p><p>Example: 1</p></td></tr><tr><td><code>attachments</code></td><td>number</td><td>The number of attachments assigned to the policy. Example: 2</td></tr></tbody></table>

## Eligibility object <a href="#eligibility" id="eligibility"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="170">Field Name</th><th width="140">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>client</code></td><td>boolean</td><td><p>Indicates direct client. </p><p>Example: true</p></td></tr><tr><td><code>partner</code></td><td>boolean</td><td><p>Indicates indirect client (partner).</p><p>Example: false</p></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
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
