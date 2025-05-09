# Journal

The Billing Journal object is linked to an authorization and is created by vendors from the available raw data from their services.

<table><thead><tr><th width="140">Field</th><th width="177">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Unique journal identifier. Note that no nesting exists for this identifier. </p><p></p><p>Example: BJO-1234-5678</p></td></tr><tr><td>name</td><td>string</td><td><p>Name of the journal. </p><p></p><p>Example: 29 Nov 2024 #1</p></td></tr><tr><td>externalId</td><td>string</td><td><p>External identifier or reference number. This is an optional value to assist vendors in matching the journal with external ERP systems.</p><p></p><p>Example: bill-12345609</p></td></tr><tr><td>notes</td><td>string</td><td><p>Journal notes added by vendor during creation of a journal. </p><p></p><p>Example: This is new billing data for November.</p></td></tr><tr><td>status</td><td>JournalStatus enum</td><td><p>State machine of the journal. </p><p></p><p>Example: Accepted</p></td></tr><tr><td>vendor</td><td>Account</td><td><p>Reference to the vendor account object that was completed during the creation of a journal.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>product</td><td>Product</td><td><p>Reference to the Product object.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td>authorization</td><td>Authorization</td><td><p>Reference to the Authorization object.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td>dueDate</td><td>DateTime</td><td><p>The due date of a journal. Possible values are generated according to Authorization. </p><p></p><p>Example: 2024-12-29T09:09:30.087Z</p></td></tr><tr><td>currency</td><td>string</td><td><p>The currency of the journal. </p><p></p><p>Example: EUR</p></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/account-user/">User</a></td><td><p>Reference to the User object. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.icon.svg"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with these possible entries: Created or Updated. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr><tr><td>price</td><td><a href="./#pricesummary">PriceSummary</a></td><td><p>The price summary including the aggregated price values for all journal charges. </p><p></p><p>Note that not all fields are visible to all actors. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td>upload</td><td><a href="./#journaluploadsummary">JournalUploadSummary</a></td><td><p>Journal upload summary, including the total charges and counts of split, ready, and error charges. </p><p></p><p>Only visible to SoftwareOne Operations and Vendor accounts. </p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "split": 4,  
  "ready": 144,
  "error": 6
}
</code></pre></td></tr><tr><td>processing</td><td><a href="./#processingsummary">ProcessingSummary</a></td><td><p>The journal processing summary including the total charges and counts of ready, error, split, cancelled, and completed charges. </p><p></p><p>Only visible to SoftwareOne Operations.</p><p></p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
  "error": 6,
  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr></tbody></table>

## PriceSummary <a href="#pricesummary" id="pricesummary"></a>

<table><thead><tr><th width="163">Field</th><th width="167">Type</th><th>Description</th></tr></thead><tbody><tr><td>totalPP</td><td>decimal</td><td><p>A sum of all purchase price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts. </p><p></p><p>Example: 229.8</p></td></tr><tr><td>markup</td><td>decimal</td><td><p>Average markup value among all charges in the billing object. Only visible to SoftwareOne Operations.</p><p></p><p>Example: 0.5013</p></td></tr><tr><td>margin</td><td>decimal</td><td><p>Average margin value among all charges in the billing object. Only visible to SoftwareOne Operations.</p><p></p><p>Example: 0.3339</p></td></tr><tr><td>totalSP</td><td>decimal</td><td><p>A sum of all the selling price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts. </p><p></p><p>Example: 356.7</p></td></tr></tbody></table>

## JournalUploadSummary <a href="#journaluploadsummary" id="journaluploadsummary"></a>

<table><thead><tr><th width="163">Field</th><th width="204">Type</th><th>Description</th></tr></thead><tbody><tr><td>total</td><td>integer</td><td><p>Number of charges in the billing object. </p><p></p><p>Example: 150</p></td></tr><tr><td>split</td><td>integer</td><td><p>Number of split charges. </p><p></p><p>Example: 4</p></td></tr><tr><td>ready</td><td>integer</td><td><p>Number of ready charges. </p><p></p><p>Example: 144</p></td></tr><tr><td>error</td><td>integer</td><td><p>Number of error charges. </p><p></p><p>Example: 6</p></td></tr></tbody></table>

## ProcessingSummary <a href="#processingsummary" id="processingsummary"></a>

<table><thead><tr><th width="189">Field</th><th width="143">Type</th><th>Description</th></tr></thead><tbody><tr><td>total</td><td>integer</td><td><p>Total number of charges in the billing object. </p><p></p><p>Example: 150</p></td></tr><tr><td>ready</td><td>integer</td><td><p>Number of ready charges. </p><p></p><p>Example: 140</p></td></tr><tr><td>error</td><td>integer</td><td><p>Number of error charges. </p><p></p><p>Example: 6</p></td></tr><tr><td>split</td><td>integer</td><td><p>Number of split charges. </p><p></p><p>Example: 4</p></td></tr><tr><td>cancelled</td><td>integer</td><td><p>Number of cancelled charges. </p><p></p><p>Example: 2</p></td></tr><tr><td>completed</td><td>integer</td><td><p>Number of completed charges. </p><p></p><p>Example: 0</p></td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% tabs %}
{% tab title="JOURNAL OBJECT" %}
```json
{
    "id": "BJO-1234-5678",
    "name": "29 Nov 2024 #1",
    "externalId": "bill-12345609",
    "notes": "This is new billing data for November",
    "status": "Accepted",
    "vendor": {
        "id": "ACC-1234-1234",
        "name": "Microsoft",
        "icon": "/static/ACC1234-1234/account.png"
    },
    "product": {
        "id": "PRD-1111-1111-1111",
        "name": "Microsoft Office 365 NCE",
        "icon": "/static/PRD1111-1111-1111/logo.png"
    },
    "authorization": {
        "id": "AUT-1234-4567",
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
{% endtab %}
{% endtabs %}
