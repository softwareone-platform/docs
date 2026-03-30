# Enrollment

Enrollment is a process through which a client formally registers or signs up to participate in a vendor program.&#x20;

Once the client fulfills all the necessary conditions, they are considered enrolled in the program, and a certificate is issued.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="195.3333740234375">Field Name</th><th width="155">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier for the enrollment. </p><p>Example: ENR-1234-1234</p></td></tr><tr><td><code>href</code></td><td>string</td><td><p>A reference to enrollment in the API. </p><p>Example: /v1/catalog/enrollments/PRD-1234-1234</p></td></tr><tr><td><code>certificate</code></td><td>object </td><td><p>A reference to the <a href="../certificate/"><code>certificate</code></a> object for this enrollment. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-5678",
    "href": "/program/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner"
}
</code></pre></td></tr><tr><td><code>program</code></td><td>object</td><td><p>A reference to the <a href="../"><code>program</code></a> object that the partner enrolls in. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
}
</code></pre></td></tr><tr><td><code>applicableTo</code></td><td>string</td><td>Defines the scope of the enrollment. Allowed values: <code>buyer</code> or <code>licensee</code>.</td></tr><tr><td><code>type</code></td><td>string</td><td>Defines whether the enrollment is new (first time requesting a certificate) or a change (re-enrollment). Allowed values: <code>change</code> or <code>new</code>.</td></tr><tr><td><code>buyer</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object, if the enrollment applies to a buyer. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
}
</code></pre></td></tr><tr><td><code>licensee</code></td><td>object</td><td><p>A reference to the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object, if the enrollment applies to a licensee. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "CER-1234-1234",
    "href": "v1/accounts/licensees/LIC-1234-1234-1234"
    "name": "Stark Industries Limited",
    "externalId": "WW-CON-12345678"
}
</code></pre></td></tr><tr><td><code>eligibility</code></td><td>object (<a href="./#eligibility"><code>eligibility</code></a>)</td><td><p>The configuration of the partner program. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "client": true,
  "partner": false
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the enrollment. Allowed values: <code>processing</code>, <code>failed</code>, <code>completed</code>, or <code>querying</code>.</td></tr><tr><td><code>statusNotes</code></td><td><a href="../../common-api-objects/message.md">message</a></td><td><p>Notes added during status change by vendor or vendor extensions to indicate the reason for enrollment failure or status change. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Educational certification failed"
}
</code></pre></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>Contains initial customer notes added by the Buyer during the enrollment process. Buyers can edit and add notes at any time for all order statuses. </p><p>Example: Enroll in a program to purchase the XYZ product.</p></td></tr><tr><td><code>error</code></td><td><a href="../../common-api-objects/message.md">message</a></td><td><p>The standard error object. It indicates that an error appeared during parameter validation, which can include markup. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Enrollment has invalid parameters"
}
</code></pre></td></tr><tr><td><code>assignee</code></td><td><a href="../../accounts-api/users/">user</a></td><td><p>The enrollment assignee, set by the vendor. The account must belong to the vendor account. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-3773-5838", 
  "href": "/accounts/ACC-0774-6909/users/USR-3773-5838",
  "name": "Jack Doe",
}
</code></pre></td></tr><tr><td><code>parameters.fulfillment</code></td><td>object (<a href="./#enrollment-parameter"><code>enrollmentParameter</code></a>)</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>parameters.ordering</code></td><td>object (<a href="./#enrollment-parameter"><code>enrollmentParameter</code></a>)</td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>template</code></td><td><a href="../../catalog-api/templates/">template</a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PTP-1234-4444", 
  "href": "/programs/PRG-1234-1234/templates/TPP-1234-4444",
  "name": "Succesful Activation" }
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Eligibility object <a href="#eligibility" id="eligibility"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="197">Field Name</th><th width="196">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>client</code></td><td>boolean</td><td><p>Indicates direct client. </p><p>Example: true</p></td></tr><tr><td><code>partner</code></td><td>boolean</td><td><p>Indicates indirect client (partner).</p><p>Example: false</p></td></tr></tbody></table>

## EnrollmentParameter object

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="197">Field Name</th><th width="197">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The primary identifier for the parameter. </p><p>Example: PAR-5542-1187-3130</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The display name of the parameter. </p><p>Example: Tenant ID</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The ID of the parameter in the external system. </p><p>Example: tenant_id</p></td></tr><tr><td><code>value</code></td><td>string</td><td><p>The parameter value, which can be updated.</p><p>Example: 69b73824-ce76-4866-ad47-b615ae9d8998 OR</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "addressLine1": "23 Oakley wood",
     "city": "Cork",
     "state": "Cork",
     "postalCode": "V23U58N"
}
</code></pre></td></tr><tr><td><code>displayValue</code></td><td>string</td><td><p>The parameter value (read only). </p><p>Example: 69b73824-ce76-4866-ad47-b615ae9d8998 OR 23 Oakley Wood, London.</p></td></tr><tr><td><code>constraints</code></td><td>parameterConstraints</td><td><p>Parameter constraints. </p><ul><li>When specified, it represents overridden parameter constraints.</li><li>When unspecified, the parameter constraints must be taken from the parameter definition. </li></ul><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "readonly": false,
    "hidden": true,
    "required": true
}
</code></pre></td></tr><tr><td><code>error</code></td><td>object (<a href="../../common-api-objects/message.md">message</a>)</td><td><p>The standard error object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Enrollment has invalid parameters"
}
</code></pre></td></tr></tbody></table>

## Example response

{% tabs %}
{% tab title="ENROLLMENT OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% code lineNumbers="true" %}
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
