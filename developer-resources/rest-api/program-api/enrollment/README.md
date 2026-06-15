# Enrollment

Enrollment is a process through which a client formally registers or signs up to participate in a vendor program.

Once the client fulfills all the necessary conditions, they are considered enrolled in the program, and a certificate is issued.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="216.3333740234375">Field</th><th width="119">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The identifier for the enrollment. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) Represents the enrollment in the API. </td></tr><tr><td><code>certificate</code></td><td>object, core</td><td><p>Represents the <a href="../certificate/"><code>certificate</code></a> object for this enrollment. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-5678",
    "href": "/program/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner"
}
</code></pre></td></tr><tr><td><code>program</code></td><td>object, core</td><td><p>Represents the <a href="../"><code>program</code></a> object that the partner enrolls in. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
}
</code></pre></td></tr><tr><td><code>applicableTo</code></td><td>string, core</td><td>Defines the scope of the enrollment. Allowed values are <code>buyer</code> or <code>licensee</code>.</td></tr><tr><td><code>type</code></td><td>string, core</td><td>Defines whether the enrollment is new (first time requesting a certificate) or a change (re-enrollment). Allowed values are <code>change</code> or <code>new</code>.</td></tr><tr><td><code>buyer</code></td><td>object, core</td><td><p>(Optional) Represents the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object, if the enrollment applies to a buyer. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
}
</code></pre></td></tr><tr><td><code>licensee</code></td><td>object, core</td><td><p>(Optional) Represents the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object, if the enrollment applies to a licensee. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "CER-1234-1234",
    "href": "v1/accounts/licensees/LIC-1234-1234-1234"
    "name": "Stark Industries Limited",
    "externalId": "WW-CON-12345678"
}
</code></pre></td></tr><tr><td><code>eligibility</code></td><td>object, core</td><td><p>The <a href="./#eligibility"><code>eligibility</code></a> object containing the configuration of the partner program. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "client": true,
  "partner": false
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The enrollment status. Allowed values are:</p><ul><li><code>Processing</code></li><li><code>Failed</code></li><li><code>Completed</code></li><li><code>Querying</code></li></ul></td></tr><tr><td><code>statusNotes</code></td><td>object</td><td><p>(Optional) Notes added during a status change by the vendor or extensions, indicating the reason for enrollment failure or status change.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Educational certification failed"
}
</code></pre></td></tr><tr><td><code>notes</code></td><td>string</td><td>(Optional) Contains initial customer notes added by the Buyer during the enrollment process. Buyers can edit and add notes at any time for all order statuses. </td></tr><tr><td><code>error</code></td><td>object</td><td><p>(Optional) The standard error object, indicating that an error occurred during parameter validation. May include markup.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Enrollment has invalid parameters"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td>object</td><td><p>(Optional) The enrollment assignee, set by the vendor. The account must belong to the vendor account. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-3773-5838", 
  "href": "/accounts/ACC-0774-6909/users/USR-3773-5838",
  "name": "Jack Doe",
}
</code></pre></td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td><p>(Optional) Represents the <a href="./#enrollment-parameter"><code>enrollmentParameter</code></a> object, which holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tenant_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }
]
</code></pre></td></tr><tr><td><code>parameters.ordering</code></td><td>object</td><td><p>(Optional) Represents the <a href="./#enrollment-parameter"><code>enrollmentParameter</code></a> object, which holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Microsoft Partner Number",
      "externalId": "partner_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }
]
</code></pre></td></tr><tr><td><code>template</code></td><td>object</td><td><p>(Optional) Represents the <a href="../../catalog-api/templates/"><code>template</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PTP-1234-4444", 
  "href": "/programs/PRG-1234-1234/templates/TPP-1234-4444",
  "name": "Successful Activation" }
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Eligibility object <a href="#eligibility" id="eligibility"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="197">Name</th><th width="116">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>client</code></td><td>boolean</td><td>Indicates direct client. </td></tr><tr><td><code>partner</code></td><td>boolean</td><td>Indicates indirect client or partner.</td></tr></tbody></table>

## Enrollment Parameter object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="197">Name</th><th width="123">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The primary identifier for the parameter. </td></tr><tr><td><code>name</code></td><td>string</td><td>The display name of the parameter. </td></tr><tr><td><code>externalId</code></td><td>string</td><td>The ID of the parameter in the external system. </td></tr><tr><td><code>value</code></td><td>string</td><td><p>The parameter value, which can be updated.</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "addressLine1": "23 Oakley wood",
     "city": "Cork",
     "state": "Cork",
     "postalCode": "V23U58N"
}
</code></pre></td></tr><tr><td><code>displayValue</code></td><td>string</td><td>The parameter value (read only). </td></tr><tr><td><code>constraints</code></td><td>object</td><td><p>Represents constraints. </p><ul><li>When specified, it represents overridden parameter constraints.</li><li>When unspecified, the parameter constraints must be taken from the parameter definition.</li></ul></td></tr><tr><td><code>error</code></td><td>object</td><td>Represents the error <a href="../../../api-usage-and-reference/common-api-objects/message.md"><code>messag</code>e</a> object.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="ENROLLMENT OBJECT" %}
{% code title="ENROLLMENT OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "ENR-1234-1234",
  "href": "/v1/products/PRD-1234-1234",
  "certificate": {
    "id": "CER-1234-1234",
    "href": "v1/catalog/certificates/CER-1234-1234"
  },
  "program": {
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
  },
  "applicableTo": "Buyer",
  "buyer": {
    "id": "BUY-1234-1234",
    "href": "v1/accounts/buyers/BUY-1234-1234",
    "name": "MPN EU"
  },
  "eligibility": {
    "client": true,
    "partner": true
  },
  "status": "Processing",
  "notes": "draft enrollment for review",
  "assignee": "",
  "parameters.fulfillment": [
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tennant Id",
      "externalId": "tenant_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }],
  "parameters.ordering": []
}
    
```
{% endcode %}
{% endtab %}

{% tab title="ENROLLMENT PARAMETER OBJECT" %}
{% code title="THE ENROLLMENT PARAMETER OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "PAR-1234-1234-1234-1234",
    "name": "Tennant Id",
    "externalId": "tenant_id",
    "constraints": {
        "readonly": false,
        "hidden": true,
        "required": true
    },
    "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
    "error": {
        "id": "E001234",
        "message": "Incorrect parameter value"
    }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
