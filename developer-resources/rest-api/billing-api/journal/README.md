# Journal

The Journal object is linked to an authorization and is created by vendors from the raw data available from their services.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="142">Field Name</th><th width="204">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the journal. No nesting exists for this identifier.</p><p>Example: BJO-1234-5678</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the journal.</p><p>Example: 29 Nov 2024 #1</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The external identifier or reference number. This is an optional value to assist vendors in matching the journal with external ERP systems.</p><p>Example: bill-12345609</p></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>Journal notes added by the vendor when creating the journal.</p><p>Example: This is new billing data for November.</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the journal. Allowed values:  <code>draft</code>, <code>deleted</code>, <code>validating</code>, <code>validated</code>, <code>error</code>, <code>ready</code>, <code>review</code>, <code>enquiring</code>, <code>generating</code>, <code>generated</code>, <code>accepted</code>, or <code>completed</code>.</td></tr><tr><td><code>vendor</code></td><td>object </td><td><p>A reference to the vendor <a href="../../accounts-api/account/"><code>account</code></a> object completed during the creation of a journal.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>authorization</code></td><td>object</td><td><p>A reference to the <a href="../../catalog-api/authorization/"><code>authorization</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td><code>dueDate</code></td><td>dateTime</td><td><p>The due date of a journal. Allowed values are generated according to <code>authorization</code>.</p><p>Example: 2024-12-29T09:09:30.087Z</p></td></tr><tr><td><code>currency</code></td><td>string</td><td><p>The currency of the journal.</p><p>Example: EUR</p></td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/account-user/"><code>user</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.icon.svg"
}  
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values: <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>The <a href="./#pricesummary"><code>priceSummary</code></a> including the aggregated price values for all journal charges. Not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td><code>upload</code></td><td>object</td><td><p>The <a href="./#journaluploadsummary"><code>journalUploadSummary</code></a>, including the total charges and counts of split, ready, and error charges. Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "split": 4,  
  "ready": 144,
  "error": 6
}
</code></pre></td></tr><tr><td><code>processing</code></td><td>object</td><td><p>The <a href="./#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges. Only visible to SoftwareOne Operations.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>

## Price Summary object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="163">Field Name</th><th width="167">Data Type</th><th width="418">Description</th></tr></thead><tbody><tr><td><code>totalPP</code></td><td>decimal</td><td><p>A sum of all purchase price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example: 229.8</p></td></tr><tr><td><code>markup</code></td><td>decimal</td><td><p>The average markup value among all charges in the billing object. Only visible to SoftwareOne Operations.</p><p>Example: 0.5013</p></td></tr><tr><td><code>margin</code></td><td>decimal</td><td><p>The average margin value among all charges in the billing object. Only visible to SoftwareOne Operations.</p><p>Example: 0.3339</p></td></tr><tr><td><code>totalSP</code></td><td>decimal</td><td><p>A sum of all the selling price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example: 356.7</p></td></tr></tbody></table>

## Journal Upload Summary object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="163">Field Name</th><th width="165">Data Type</th><th width="381">Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>integer</td><td><p>The number of charges in the billing object.</p><p>Example: 150</p></td></tr><tr><td><code>split</code></td><td>integer</td><td><p>The number of split charges.</p><p>Example: 4</p></td></tr><tr><td><code>ready</code></td><td>integer</td><td><p>The number of ready charges.</p><p>Example: 144</p></td></tr><tr><td><code>error</code></td><td>integer</td><td><p>The number of error charges.</p><p>Example: 6</p></td></tr></tbody></table>

## Processing Summary object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="167">Field Name</th><th width="161">Data Type</th><th width="416">Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>integer</td><td><p>The total number of charges within the billing object.</p><p>Example: 150</p></td></tr><tr><td><code>ready</code></td><td>integer</td><td><p>The total number of ready charges.</p><p>Example: 140</p></td></tr><tr><td><code>error</code></td><td>integer</td><td><p>The total number of error charges.</p><p>Example: 6</p></td></tr><tr><td><code>split</code></td><td>integer</td><td><p>The total number of split charges.</p><p>Example: 4</p></td></tr><tr><td><code>cancelled</code></td><td>integer</td><td><p>The total number of cancelled charges.</p><p>Example: 2</p></td></tr><tr><td><code>completed</code></td><td>integer</td><td><p>The total number of completed charges.</p><p>Example: 0</p></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
    "id": "BJO-1234-5678",
    "name": "29 Nov 2024 #1",
    "externalId": "bill-12345609",
    "notes": "This is new billing data for November",
    "status": "Accepted",
    "vendor": {
        "id": "ACC-1234-1234",
        "href": "/accounts/accounts/ACC-1234-1234",
        "name": "Microsoft",
        "icon": "/static/ACC1234-1234/account.png"
    },
    "product": {
        "id": "PRD-1111-1111-1111",
        "href": "/catalog/products/PRD-1111-1111-1111",
        "name": "Microsoft Office 365 NCE",
        "icon": "/static/PRD1111-1111-1111/logo.png"
    },
    "authorization": {
        "id": "AUT-1234-4567",
        "href": "/authorization/ATH-1234-45678",
        "name": "Salesforce Enterprise License"
    },
    "dueDate": "2024-12-29T09:09:30.087Z",
    "currency": "EUR",
    "assignee": {
        "id": "USR-1234-1234-1234",
        "name": "John Smith",
        "icon": "/static/users/USR-1234-1234-1234.icon.svg"
    },
    "audit": {
        "created": {
            "at": "...",
            "by": {}
        },
        "updated": {
            "at": "...",
            "by": {}
        }
    },
    "priceSummary": {
        "totalPP": 229.8,
        "markup": 0.5013,
        "margin": 0.3339,
        "totalSP": 356.7
    },
    "uploadSummary": {
        "total": 150,
        "split": 4,
        "ready": 144,
        "error": 6
    },
    "processingSummary": {
        "total": 150,
        "ready": 140,
        "error": 6,
        "split": 4,
        "cancelled": 2,
        "completed": 0
    }
}
```
{% endcode %}
