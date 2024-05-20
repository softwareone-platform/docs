# Listings

## Listing object

The `Listing` object represents a business object that positions a Product within the purview of a particular SoftwareOne seller, characterized by a specific Authorization and an assigned Price List. Listings play a crucial role in controlling the visibility and availability of Products in various markets and managing their lifecycle in a scalable and efficient manner.

| Field         | Type                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------- | ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id            | string                                    | Primary listing identifier                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| href          | string                                    | <p>Relative reference to object on API (always <code>/listing/{id}</code>). </p><p></p><p>Example: "LST-1234-4678"</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| product       | [Product](../product/#product-object)     | <p>Reference to <a href="../product/#product-object">Product</a> object. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRD-1111-1111",
    "href": "/products/PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111/logo.png"
}
</code></pre>                                                                                                                                                                                                                            |
| authorization | [Authorization](../authorizations/)       | <p>Reference to <a href="../authorizations/">Authorization</a> object. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "AUT-1234-4567",
    "href": "/authorization/ATH-1234-45678",
    "name": "Salesforce Enterprise License"
}
</code></pre>                                                                                                                                                                                                                                                                 |
| seller        | [Seller](../../accounts-api/seller/)      | <p>Reference to <a href="../../accounts-api/seller/">Seller</a> object. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "SEL-1234-4567",
    "href": "/seller/SEL-1234-45678",
    "name": "SoftwareOne, Inc."
}
</code></pre>                                                                                                                                                                                                                                                                                   |
| priceList     | [PriceList](../price-lists/)              | <p>Reference to <a href="../price-lists/">PriceList</a> object. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
    "id": "PRC-1234-5678-1234,
    "href": "/price-list/PRC-1234-5678-1234
}
</code></pre>                                                                                                                                                                                                                                                                                                                 |
| primary       | boolean                                   | <p>If product has more associated listings with the same seller, the “primary” flag is used to indicate which listing is used in purchase wizard. </p><p></p><p>Example: "true"</p>                                                                                                                                                                                                                                                                                                                                                                                         |
| notes         | string                                    | <p>Any user notes about the Listing.</p><p></p><p>Example: "This is the primary Listing for the EU region"</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| statistics    | [ListingStatistics](./#listingstatistics) | <p>System calculated metrics about the Listing. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "subscriptionCount": 10,
  "agreementCount": 5
}
</code></pre>                                                                                                                                                                                                                                                                                                                                                           |
| audit         | AuditObject                               | <p>Audit object with possible entries: created, updated, activated, terminated, according to lifecycle of the object. Possible audit events: <strong>created</strong>, <strong>updated</strong>, <strong>activated</strong>, <strong>terminated</strong>, <strong>failed</strong>. </p><p></p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "activated": { "at": "...", "by": { } },
  "terminated": { "at": "...", "by": { } }
}
</code></pre> |

## ListingStatistics <a href="#listingstatistics" id="listingstatistics"></a>

| subscriptions | int | <p>Number of associated subscriptions. </p><p></p><p>Example: "10"</p> |
| ------------- | --- | ---------------------------------------------------------------------- |
| agreements    | int | <p>Number of associated agreements </p><p></p><p>Example: "5"</p>      |

## Example

{% tabs %}
{% tab title="LISTING OBJECT" %}
```json
{
  "id": "LST-1234-4678",
  "href": "/listing/LST-1234-4678",
  "product": {
    "id": "PRD-1111-1111",
    "href": "/products/PRD-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111/logo.png"
  },
  "authorization": {
    "id": "AUT-1234-4567",
    "href": "/authorization/ATH-1234-45678",
    "name": "Salesforce Enterprise License"
  }, 
  "seller": {
    "id": "SEL-1234-45678",
    "href": "/seller/SEL-1234-4567",
    "name": "SoftwareOne, Inc."
  },
  "priceList": {
    "id": "PRC-1234-5678-1234",
    "href": "/price-list/PRC-1234-5678-1234"
  },
  "primary": true,
  "notes": "This is the primary Listing for the EU region.",
  "statistics": {
    "subscriptions": 10,
    "agreements": 5
  },
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  },
}
```
{% endtab %}
{% endtabs %}
