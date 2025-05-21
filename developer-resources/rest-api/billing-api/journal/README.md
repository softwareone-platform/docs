# Journal

The Journal object is linked to an authorization and is created by vendors from the raw data available from their services.

<table><thead><tr><th width="134">Field</th><th width="204">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>A unique identifier for the journal. Note that no nesting exists for this identifier.</p><p>Example: BJO-1234-5678</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the journal.</p><p>Example: 29 Nov 2024 #1</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The external identifier or reference number. This is an optional value to assist vendors in matching the journal with external ERP systems.</p><p>Example: bill-12345609</p></td></tr><tr><td>notes</td><td><code>string</code></td><td><p>The journal notes added by the vendor during the creation of the journal.</p><p>Example: This is new billing data for November.</p></td></tr><tr><td>status</td><td><code>enum</code></td><td>Journal's status. Possible values: <code>Draft</code>, <code>Deleted</code>, <code>Validating</code>, <code>Validated</code>, <code>Error</code>, <code>Ready</code>, <code>Review</code>, <code>Enquiring</code>, <code>Generating</code>, <code>Generated</code>, <code>Accepted</code>, or <code>Completed</code>.</td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the vendor account object completed during the creation of a journal.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>product</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>A reference to the Product object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>authorization</td><td><a href="../../catalog-api/authorization/"><code>authorization</code></a></td><td><p>A reference to the Authorization object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td>dueDate</td><td><code>dateTime</code></td><td><p>The due date of a journal. Possible values are generated according to Authorization.</p><p>Example: 2024-12-29T09:09:30.087Z</p></td></tr><tr><td>currency</td><td><code>string</code></td><td><p>The currency of the journal.</p><p>Example: EUR</p></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/account/account-user/"><code>user</code></a></td><td><p>A reference to the User object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.icon.svg"
}  
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>A reference to the Audit object. </p><p>Possible values: <code>Created</code> or <code>Updated</code>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>price</td><td><a href="./#pricesummary"><code>priceSummary</code></a></td><td><p>The price summary including the aggregated price values for all journal charges.</p><p>Note that not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td>upload</td><td><a href="./#journaluploadsummary"><code>journalUploadSummary</code></a></td><td><p>The journal upload summary, including the total charges and counts of split, ready, and error charges.</p><p>Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "total": 150,
  "split": 4,  
  "ready": 144,
  "error": 6
}
</code></pre></td></tr><tr><td>processing</td><td><a href="./#processingsummary"><code>processingSummary</code></a></td><td><p>The journal processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges. </p><p>Only visible to SoftwareOne Operations.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>

## PriceSummary

<table><thead><tr><th width="163">Field</th><th width="167">Type</th><th width="418">Description</th></tr></thead><tbody><tr><td>totalPP</td><td><code>decimal</code></td><td><p>A sum of all purchase price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example: 229.8</p></td></tr><tr><td>markup</td><td><code>decimal</code></td><td><p>The average markup value among all charges in the billing object. Only visible to SoftwareOne Operations.</p><p>Example: 0.5013</p></td></tr><tr><td>margin</td><td><code>decimal</code></td><td><p>The average margin value among all charges in the billing object. Only visible to SoftwareOne Operations.</p><p>Example: 0.3339</p></td></tr><tr><td>totalSP</td><td><code>decimal</code></td><td><p>A sum of all the selling price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example: 356.7</p></td></tr></tbody></table>

## JournalUploadSummary

<table><thead><tr><th width="163">Field</th><th width="165">Type</th><th width="381">Description</th></tr></thead><tbody><tr><td>total</td><td><code>integer</code></td><td><p>The number of charges in the billing object.</p><p>Example: 150</p></td></tr><tr><td>split</td><td><code>integer</code></td><td><p>The number of split charges.</p><p>Example: 4</p></td></tr><tr><td>ready</td><td><code>integer</code></td><td><p>The number of ready charges.</p><p>Example: 144</p></td></tr><tr><td>error</td><td><code>integer</code></td><td><p>The number of error charges.</p><p>Example: 6</p></td></tr></tbody></table>

## ProcessingSummary

<table><thead><tr><th width="167">Field</th><th width="161">Type</th><th width="416">Description</th></tr></thead><tbody><tr><td>total</td><td><code>integer</code></td><td><p>The total number of charges within the billing object.</p><p>Example: 150</p></td></tr><tr><td>ready</td><td><code>integer</code></td><td><p>The total number of ready charges.</p><p>Example: 140</p></td></tr><tr><td>error</td><td><code>integer</code></td><td><p>The total number of error charges.</p><p>Example: 6</p></td></tr><tr><td>split</td><td><code>integer</code></td><td><p>The total number of split charges.</p><p>Example: 4</p></td></tr><tr><td>cancelled</td><td><code>integer</code></td><td><p>The total number of cancelled charges.</p><p>Example: 2</p></td></tr><tr><td>completed</td><td><code>integer</code></td><td><p>The total number of completed charges.</p><p>Example: 0</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="JOURNAL OBJECT" %}
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
{% endtab %}
{% endtabs %}

Journal object

<table data-header-hidden><thead><tr><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><p>{</p><p>"id": "BJO-1234-5678",</p><p>"name": "29 Nov 2024 #1",</p><p>"externalId": "bill-12345609",</p><p>"notes": "This is new billing data for November",</p><p>"status": "Accepted",</p><p>"vendor": {</p><p>"id": "ACC-1234-1234",</p><p>"name": "Microsoft",</p><p>"icon": "/static/ACC1234-1234/account.png"</p><p>},</p><p>"product": {</p><p>"id": "PRD-1111-1111-1111",</p><p>"name": "Microsoft Office 365 NCE",</p><p>"icon": "/static/PRD1111-1111-1111/logo.png"</p><p>},</p><p>"authorization": {</p><p>"id": "AUT-1234-4567",</p><p>"name": "Salesforce Enterprise License"</p><p>},</p><p>"dueDate": "2024-12-29T09:09:30.087Z",</p><p>"currency": "EUR",</p><p>"assignee": {</p><p>"id": "USR-1234-1234-1234",</p><p>"name": "John Smith",</p><p>"icon": "/static/users/USR-1234-1234-1234.icon.svg"</p><p>},</p><p>"audit": {</p><p>"created": {</p><p>"at": "...",</p><p>"by": {}</p><p>},</p><p>"updated": {</p><p>"at": "...",</p><p>"by": {}</p><p>}</p><p>},</p><p>"priceSummary": {</p><p>"totalPP": 229.8,</p><p>"markup": 0.5013,</p><p>"margin": 0.3339,</p><p>"totalSP": 356.7</p><p>},</p><p>"uploadSummary": {</p><p>"total": 150,</p><p>"split": 4,</p><p>"ready": 144,</p><p>"error": 6</p><p>},</p><p>"processingSummary": {</p><p>"total": 150,</p><p>"ready": 140,</p><p>"error": 6,</p><p>"split": 4,</p><p>"cancelled": 2,</p><p>"completed": 0</p><p>}</p><p>}</p><p> </p></td></tr></tbody></table>
