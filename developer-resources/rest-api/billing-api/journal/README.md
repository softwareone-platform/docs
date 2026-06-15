# Journal

The Journal object is linked to an authorization and is created by vendors from the raw data available from their services.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="142">Field</th><th width="169">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) A unique identifier for the journal. No nesting exists for this identifier.</td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the journal.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>(Optional) The external identifier or reference number. This is an optional value to assist vendors in matching the journal with external ERP systems.</td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) Journal notes added by the vendor when creating the journal.</td></tr><tr><td><code>status</code></td><td>enum</td><td><p>(Read-only) The status of the journal. Allowed values are:  </p><ul><li><code>Draft</code></li><li><code>Deleted</code></li><li><code>Validating</code></li><li><code>Validated</code></li><li><code>Error</code></li><li><code>Ready</code></li><li><code>Review</code></li><li><code>Enquiring</code></li><li><code>Generating</code></li><li><code>Generated</code></li><li><code>Accepted</code></li><li><code>Completed</code></li></ul></td></tr><tr><td><code>vendor</code></td><td>object </td><td><p>(Read-only) Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object completed during the creation of a journal.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>product</code></td><td>object</td><td><p>Represents the <a href="../../catalog-api/product/"><code>product</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRD-1111-1111-1111",
    "name": "Microsoft Office 365 NCE",
    "icon": "/static/PRD-1111-1111-1111/logo.png"
}
</code></pre></td></tr><tr><td><code>authorization</code></td><td>object</td><td><p>Represents the <a href="../../catalog-api/authorization/"><code>authorization</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "AUT-1234-4567",
    "name": "Salesforce Enterprise License"
}
</code></pre></td></tr><tr><td><code>dueDate</code></td><td>dateTime, core</td><td>The due date of a journal. Allowed values are generated according to <code>authorization</code>.</td></tr><tr><td><code>currency</code></td><td>string</td><td>The currency of the journal.</td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>(Optional) Represents the <a href="../../accounts-api/account-user/"><code>user</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-1234-1234-1234",
  "name": "John Smith",
  "icon": "/static/users/USR-1234-1234-1234.icon.svg"
}  
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. Allowed values are <code>created</code> or <code>updated</code>.</td></tr><tr><td><code>price</code></td><td>object</td><td><p>(Read-only) The <a href="./#pricesummary"><code>priceSummary</code></a> including the aggregated price values for all journal charges. Not all fields are visible to all actors.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "totalPP": 229.8,
  "markup": 0.5013,
  "margin": 0.3339,  
  "totalSP": 356.7
}
</code></pre></td></tr><tr><td><code>upload</code></td><td>object</td><td><p>(Read-only) The <a href="./#journaluploadsummary"><code>journalUploadSummary</code></a>, including the total charges and counts of split, ready, and error charges. Only visible to SoftwareOne Operations and Vendor accounts.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "split": 4,  
  "ready": 144,
  "error": 6
}
</code></pre></td></tr><tr><td><code>processing</code></td><td>object</td><td><p>(Read-only) The <a href="./#processingsummary"><code>processingSummary</code></a> including the total charges and counts of ready, error, split, cancelled, and completed charges. Only visible to SoftwareOne Operations.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "total": 150,
  "ready": 140,
<strong>  "error": 6,
</strong>  "split": 4,
  "cancelled": 2,
  "completed": 0    
}
</code></pre></td></tr><tr><td><code>error</code></td><td>object</td><td>(Read-only) (Optional) Represents the <code>billingEntityError</code> object containing error details associated with the journal entry, if any.</td></tr></tbody></table>

## Single Currency Price Summary object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="134">Field</th><th width="132">Type</th><th width="418">Description</th></tr></thead><tbody><tr><td><code>totalPP</code></td><td>decimal</td><td>(Read-only) A sum of all purchase price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</td></tr><tr><td><code>markup</code></td><td>decimal</td><td>(Read-only)The average markup value among all charges in the billing object. Only visible to SoftwareOne Operations.</td></tr><tr><td><code>margin</code></td><td>decimal</td><td>(Read-only) The average margin value among all charges in the billing object. Only visible to SoftwareOne Operations.</td></tr><tr><td><code>totalBSP</code></td><td>decimal</td><td>(Read-only) A sum of all the selling price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</td></tr></tbody></table>

## Multi Currency Price Summary object

<table><thead><tr><th width="172">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td>currency</td><td>object</td><td><p>(Read-only) Purchase and sale currency with conversion rate.  </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "purchase": "EUR",
  "sale": "USD",  
  "rate": 0.83
}
</code></pre></td></tr><tr><td>markup</td><td>decimal</td><td>(Read-only) Average markup value among all charges in the billing object. Only visible to SoftwareOne Operations.</td></tr><tr><td>margin</td><td>decimal</td><td>(Read-only) Average margin value among all charges in the billing object. Only visible to SoftwareOne Operations.</td></tr><tr><td>totalPP</td><td>decimal</td><td>(Read-only) Sum of all purchase price values of all charges in the billing object. Only visible to SoftwareOne Operations and Vendor accounts.</td></tr><tr><td>totalBSP</td><td>decimal</td><td>(Read-only) Sum of all BSP values of all charges in the billing object. Only visible to SoftwareOne Operations and Client accounts.</td></tr><tr><td>totalSP</td><td>decimal</td><td>(Read-only) Sum of all sell price values of all charges in the billing object. Only visible to SoftwareOne Operations and Client accounts</td></tr></tbody></table>

## Price Currency object

<table><thead><tr><th width="128">Field</th><th width="125">Type</th><th width="418">Description</th></tr></thead><tbody><tr><td><code>purchase</code></td><td>sting</td><td>A reference to the purchase currency.</td></tr><tr><td><code>sale</code></td><td>sting</td><td>A reference to the sale currency.</td></tr><tr><td><code>rate</code></td><td>decimal</td><td>(Read-only) A conversion rate between purchase and sale currency.</td></tr></tbody></table>

## Journal Upload Summary object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="137">Field</th><th width="122">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>integer</td><td>(Read-only) Number of charges in the billing object.</td></tr><tr><td><code>split</code></td><td>integer</td><td>(Read-only) Number of split charges.</td></tr><tr><td><code>ready</code></td><td>integer</td><td>(Read-only) Number of ready charges.</td></tr><tr><td><code>error</code></td><td>integer</td><td>(Read-only) Number of error charges.</td></tr></tbody></table>

## Processing Summary object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="137">Field</th><th width="145">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>total</code></td><td>integer</td><td>(Read-only) The total number of charges within the billing object.</td></tr><tr><td><code>ready</code></td><td>integer</td><td>(Read-only) The total number of ready charges.</td></tr><tr><td><code>error</code></td><td>integer</td><td>(Read-only) The total number of error charges.</td></tr><tr><td><code>split</code></td><td>integer</td><td>(Read-only) The total number of split charges.</td></tr><tr><td><code>cancelled</code></td><td>integer</td><td>(Read-only) The total number of cancelled charges.</td></tr><tr><td><code>completed</code></td><td>integer</td><td>(Read-only) The total number of completed charges.</td></tr></tbody></table>

## Example

{% code title="JOURNAL OBJECT" lineNumbers="true" %}
```json
{
    "id": "BJO-1234-5678",
    "name": "29 Nov 2024 #1",
    "externalIds": {
      "vendor": "bill-12345609",
      "operations": "SO-1234-1234-1111"
    },
    "notes": "This is new billing data for November",
    "status": "Accepted",
    "vendor": {
        "id": "ACC-9566-7072",
        "type": "Vendor",
        "status": "Active",
        "name": "Vikings"
    },
    "owner": {
        "id": "SEL-0209-5314",
        "address": {
            "country": "PL"
        },
        "name": "20 Adam's buyer",
        "icon": "/v1/accounts/sellers/SEL-0209-5314/icon"
    },  
    "product": {
        "id": "PRD-5771-7575",
        "name": "Valhalla",
        "externalIds": {},
        "icon": "/v1/catalog/products/PRD-5771-7575/icon",
        "status": "Published"
    },
    "authorization": {
        "id": "AUT-4320-7499",
        "name": "Vikings",
        "currency": "EUR"
    },
    "dueDate": "2024-12-29T09:09:30.087Z",
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
        "totalSP": 356.7,
        "currency": "EUR",
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
        "skipped": 2
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
