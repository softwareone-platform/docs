# Pricing Policies

The Pricing Policy object contains the following attributes:

<table><thead><tr><th width="116">Field</th><th width="227">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td>The identifier of the pricing policy.</td></tr><tr><td>client</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td>The client to whom the pricing policy belongs.</td></tr><tr><td>markup</td><td><code>decimal</code></td><td>The markup that has been applied to the yield cap. Optional on request: if omitted, the markup requires a margin to be provided. Only SoftwareOne operations can view this field. Example: 0.5013</td></tr><tr><td>margin</td><td><code>decimal</code></td><td><p>The margin of the yield cap. Optional on request: if omitted, the markup requires a margin to be provided. Only SoftwareOne operations can view this field. </p><p>Example: 0.3339</p></td></tr><tr><td>products</td><td><a href="../product/"><code>product</code></a></td><td><p>Contains a list of selected products. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "PRD-1111-1111-1111",    
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
  }
]
</code></pre></td></tr><tr><td>status</td><td><code>enum</code></td><td><p>Indicates the status of the price policy. The</p><p>possible values are <code>Active</code>, <code>Disabled</code>, or <code>Deleted</code>.</p></td></tr><tr><td>eligibility</td><td><code>decimal</code></td><td><p>Indicates whether the policy applies to clients (Tier 1), partners (Tier 2), or both. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  "client": true,
  "partner": false
]
</code></pre></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the pricing policy.</p><p>Example: PRP for Stark Industries</p></td></tr><tr><td>externalIds</td><td><a href="../../common-api-objects/externalids.md"><code>externalIds</code></a></td><td>A reference to the ExternalIds object.</td></tr><tr><td>notes</td><td><code>string</code></td><td><p>User notes about the pricing policy.</p><p>Example: This is the primary pricing policy for the EU.</p></td></tr><tr><td>statistics</td><td><a href="./#pricingpolicystatistics-object"><code>pricingPolicyStatistics</code></a></td><td>A reference to the PricingPolicyStatistics object.</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object. </td></tr></tbody></table>

## Pricing Policy Attachment Object <a href="#pricingpolicyattachment-object" id="pricingpolicyattachment-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="173">Field</th><th width="123">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The ID of the attachment. </p><p>Example: PPA-1234-1222-1234-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the attachment. </p><p>Example: Pricing policy negotiation 2025</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of file.</p><p>Example: Text</p></td></tr><tr><td>size</td><td><code>integer</code></td><td><p>The size of the file.</p><p>Example: 123</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>A description of the attachment. </p><p>Example: This policy outlines the negotiated pricing terms between SoftwareOne and Stark Industries, established in August 2025. It details the specific pricing policies tailored to the needs of both parties.</p></td></tr><tr><td>fileName</td><td><code>string</code></td><td><p>The name of the file.</p><p>Example: 01984827423.pdf</p></td></tr><tr><td>contentType</td><td><code>string</code></td><td><p>Indicates the content type. </p><p>Example: application/x-pdf</p></td></tr><tr><td>status</td><td><code>enum</code></td><td>Indicates the status of the pricing policy attachment. Example: Active</td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the Audit object. </td></tr></tbody></table>

## Pricing Policy Statistics Object <a href="#pricingpolicystatistics-object" id="pricingpolicystatistics-object"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="168">Field</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>orders</td><td><code>number</code></td><td><p>The number of orders assigned to the policy. </p><p>Example: 1</p></td></tr><tr><td>attachments</td><td><code>number</code></td><td>The number of attachments assigned to the policy. Example: 2</td></tr></tbody></table>

## Eligibility <a href="#eligibility" id="eligibility"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="170">Field</th><th width="140">Type</th><th>Description</th></tr></thead><tbody><tr><td>client</td><td><code>boolean</code></td><td><p>Indicates direct client. </p><p>Example: true</p></td></tr><tr><td>partner</td><td><code>boolean</code></td><td><p>Indicates indirect client (partner).</p><p>Example: false</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PRICING POLICY" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
