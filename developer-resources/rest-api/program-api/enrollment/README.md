# Enrollments

Enrollment is a process through which a client or entity formally registers or signs up to participate in a vendor program.&#x20;

Once the client fulfills all the necessary conditions, they are considered enrolled in the program, and a certificate is issued.

<table><thead><tr><th width="198">Field</th><th width="193">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier for the enrollment. </p><p>Example: ENR-1234-1234</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>A reference to enrollment in the API. </p><p>Example: /v1/catalog/enrollments/PRD-1234-1234</p></td></tr><tr><td>certificate</td><td><a href="../certificate/"><code>certificate</code></a></td><td><p>A reference to the Certificate object for this enrollment. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-5678",
    "href": "/program/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner"
}
</code></pre></td></tr><tr><td>program</td><td><a href="../"><code>program</code></a></td><td><p>A reference to the Program object that the partner enrolls in. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
}
</code></pre></td></tr><tr><td>applicableTo</td><td><code>string</code></td><td><p>Defines the scope of the enrollment. </p><p>Possible values: <code>Buyer</code> or <code>Licensee</code>.</p></td></tr><tr><td>type</td><td><code>string</code></td><td>Defines if enrollment is new (first time requesting a certificate) or a change (re-enrollment). Possible values: <code>Change</code> or <code>New</code>.</td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/"><code>buyer</code></a></td><td><p>A reference to the Buyer object if the enrollment applies to the buyer. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-1234",
    "href": "v1/catalog/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner",
    "icon": "/static/PRG-1234-1234/logo.png",
    "applicableTo": "Buyer"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/"><code>licensee</code></a></td><td><p>A reference to the Licensee object if the enrollment applies to the licensee. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "CER-1234-1234",
    "href": "v1/accounts/licensees/LIC-1234-1234-1234"
    "name": "Stark Industries Limited",
    "externalId": "WW-CON-12345678"
}
</code></pre></td></tr><tr><td>eligibility</td><td><a href="./#eligibility"><code>eligibility</code></a></td><td><p>The configuration of the partner program. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "client": true,
  "partner": false
}
</code></pre></td></tr><tr><td>status</td><td><code>enum</code></td><td><p>The status of the enrollment. </p><p>Possible values: <code>Processing</code>, <code>Failed</code>, <code>Completed</code>, or <code>Querying</code>.</p></td></tr><tr><td>statusNotes</td><td><a href="../../common-api-objects/message.md"><code>message</code></a></td><td><p>Notes added during status change by vendor or vendor extensions to indicate the reason for enrollment failure or status change. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Educational certification failed"
}
</code></pre></td></tr><tr><td>notes</td><td><code>string</code></td><td><p>Contains initial customer notes added by the Buyer during the enrollment process. Buyers can edit and add notes at any time for all order statuses. </p><p>Example: Enroll for a program needed to purchase product XYZ</p></td></tr><tr><td>error</td><td><a href="../../common-api-objects/message.md"><code>message</code></a></td><td><p>The standard error object. It indicates that an error appeared during parameter validation, which can include markup. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Enrollment has invalid parameters"
}
</code></pre></td></tr><tr><td>assignee</td><td><a href="../../accounts-api/users/"><code>user</code></a></td><td><p>The enrollment assignee, set by the vendor. The account must belong to the vendor account. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "id": "USR-3773-5838", 
  "href": "/accounts/ACC-0774-6909/users/USR-3773-5838",
  "name": "Jack Doe",
}
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td><a href="./#enrollment-parameter"><code>enrollmentParameter</code></a></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
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
</code></pre></td></tr><tr><td>parameters.ordering</td><td><a href="./#enrollment-parameter"><code>enrollmentParameter</code></a></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
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
</code></pre></td></tr><tr><td>template</td><td><a href="../../catalog-api/templates/"><code>template</code></a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "id": "PTP-1234-4444", 
  "href": "/programs/PRG-1234-1234/templates/TPP-1234-4444",
  "name": "Succesful Activation" }
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the audit information object. </td></tr></tbody></table>

## Eligibility <a href="#eligibility" id="eligibility"></a>

<table><thead><tr><th width="197">Field</th><th width="196">Type</th><th>Description</th></tr></thead><tbody><tr><td>client</td><td><code>boolean</code></td><td><p>Indicates direct client. </p><p>Example: true</p></td></tr><tr><td>partner</td><td><code>boolean</code></td><td><p>Indicates indirect client (partner).</p><p>Example: false</p></td></tr></tbody></table>

## Enrollment Parameter

<table><thead><tr><th width="199">Field</th><th width="205">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier for the parameter. </p><p>Example: PAR-5542-1187-3130</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The display name of the parameter. </p><p>Example: Tenant ID</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The ID of the parameter in the external system. </p><p>Example: tenant_id</p></td></tr><tr><td>value</td><td><code>string</code></td><td><p>The parameter value (can be updated).</p><p>Example: 69b73824-ce76-4866-ad47-b615ae9d8998 OR</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
     "addressLine1": "23 Oakley wood",
     "city": "Cork",
     "state": "Cork",
     "postalCode": "V23U58N"
}
</code></pre></td></tr><tr><td>displayValue</td><td><code>string</code></td><td><p>The parameter value (read only). </p><p>Example: 69b73824-ce76-4866-ad47-b615ae9d8998 OR 23 Oakley Wood, London.</p></td></tr><tr><td>constraints</td><td><code>parameterConstraints</code></td><td><p>Parameter constraints. When specified, it represents overridden parameter constraints.<br>When unspecified, the parameter constraints must be taken from the parameter definition. Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "readonly": false,
    "hidden": true,
    "required": true
}
</code></pre></td></tr><tr><td>error</td><td><a href="../../common-api-objects/message.md"><code>message</code></a></td><td><p>The standard error object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "E001234",
    "message": "Enrollment has invalid parameters"
}
</code></pre></td></tr></tbody></table>

## Enrollment Attachment

The Enrollment Attachment object provides the ability to upload an enrollment attachment (via file upload or license key) to the enrollment object.

<table><thead><tr><th width="202">Field</th><th width="198">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The primary identifier of the attachment. </p><p>Example: ATT-0001-0001-0001-001</p></td></tr><tr><td>href</td><td><code>string</code></td><td> A reference to attachment within the API. </td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the attachment object.  </p><p>Example: Guide to establishing a reseller relationship</p></td></tr><tr><td>description</td><td><code>string</code></td><td><p>The description of the attachment object. </p><p>Example: Learn what happens when you establish a reseller relationship with SoftwareOne</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of the attachment object. </p><p>Example: File</p></td></tr><tr><td>reference</td><td><code>string</code></td><td><p>The URI to access the attachment object. </p><p>Example: microsoft-agreement-certification.pdf</p></td></tr><tr><td>order</td><td><code>order</code></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ORD-5542-1187-3130-0991",
    "href": "/commerce/orders/ORD-5542-1187-3130-0991"
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td>A reference to the audit object. </td></tr></tbody></table>

## Examples

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

{% tab title="ENROLLMENT ATTACHMENT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
 {
    "id": "ATT-0001-0001-0001-0001",
    "href": "v1/catalog/enrollment/attachment/ATT-0001-0001-0001-0001",
    "name": "Guide to establishing a reseller relationship",
    "description": "Learn what happens when you establish a reseller relationship with SoftwareOne",
    "type": "File",
    "reference": "microsoft-agreement-certification.pdf",
    "order": {
        "id": "ORD-5542-1187-3130-0991",
        "href": "/commerce/orders/ORD-5542-1187-3130-0991"
    },
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
  }
```
{% endcode %}
{% endtab %}
{% endtabs %}
