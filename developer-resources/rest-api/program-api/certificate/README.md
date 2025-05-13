# Certificate

A certificate is issued to a client or partner as confirmation that they meet a specific program's requirements. This document is proof that the client or partner has adhered to the vendor's standards and is now eligible to purchase or access their products. The following rules apply to certificates:

* A certificate can only be created or re-enrolled for published programs.
* A client or partner can re-enroll for a certificate if it's in **Active** or **Expired** status. Re-enrollment is not permitted for terminated certificates.
* A certificate can automatically expire on its expiration date, changing its status to **Expired**.

<table><thead><tr><th width="204">Field</th><th width="149">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The business identifier of the certificate. </p><p>Example: CER-1234-5678-9012</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>The resource URI of the certificate. </p><p>Example: /v1/program/certificates/CER-1234-5678-9012</p></td></tr><tr><td>program</td><td><code>program</code></td><td><p>The program to which this certificate applies. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-5678",
    "href": "/program/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner"
}
</code></pre></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>The client or partner to whom the certificate belongs. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1222",
    "href": "/accounts/accounts/ACC-1234-1222",
    "name": "Oscorp Industries",
    "icon": "/static/ACC-1234-1222/account.png"
}
</code></pre></td></tr><tr><td>applicableTo</td><td><code>string</code></td><td>Defines the scope in which the given enrollment has been created. Possible values: <code>Buyer</code> or <code>Licensee</code>.</td></tr><tr><td>buyer</td><td><a href="../../accounts-api/buyer/"><code>buyer</code></a></td><td><p>A reference to the Buyer object if the enrollment applies to the buyer. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "BUY-1234-1234",
    "href": "v1/accounts/buyers/BUY-1234-1234",
    "name": "MPN EU"
}
</code></pre></td></tr><tr><td>licensee</td><td><a href="../../accounts-api/licensee/"><code>licensee</code></a></td><td><p>A reference to the Licensee object if the enrollment applies to the licensee. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "CER-1234-1234",
    "href": "v1/accounts/licensees/LIC-1234-1234-1234"
    "name": "Rolls-Royce Canada Limited",
    "externalId": "WW-CON-12345678"
}
</code></pre></td></tr><tr><td>eligibility</td><td><code>eligibility</code></td><td><p>Configuration of the partner program.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "client": true,
  "partner": false
}
</code></pre></td></tr><tr><td>externalIds</td><td><code>externalIds</code></td><td><p>Identifier for the external system.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "vendor": "ven-1233-3222"
}
</code></pre></td></tr><tr><td>status</td><td><code>string</code></td><td><p>The certificate's status. </p><p>Possible values: <code>Pending</code>, <code>Updating</code>, <code>Active</code>, <code>Terminated</code>, or <code>Expired</code>.</p></td></tr><tr><td>expirationDate</td><td><code>dateTime</code></td><td><p>The expiration date of the certificate. </p><p>When the date has passed, the system expires the certificate. </p><p>Example: 2025-12-04</p></td></tr><tr><td>template</td><td><a href="../../catalog-api/templates/">template</a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{ 
  "id": "PTP-1234-4444", 
  "href": "/programs/PRG-1234 1234/templates/TPP-1234-4444",
  "name": "Succesful Activation" }
</code></pre></td></tr><tr><td>parameters.fulfillment</td><td><a href="../enrollment/#enrollment-parameter"><code>orderParameter</code></a></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tenant Id",
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
</code></pre></td></tr><tr><td>parameters.ordering</td><td><a href="../enrollment/#enrollment-parameter"><code>orderParameter</code></a></td><td><p>An object that holds a concise definition of a parameter, its value, and any associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tenant Id",
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
</code></pre></td></tr><tr><td>audit</td><td><code>auditObject</code></td><td><p>The audit information object. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Parameter Value <a href="#parametervalue" id="parametervalue"></a>

<table><thead><tr><th width="169">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The identifier of the parameter definition this value refers to. </p><p>Example: PAR-1234-1234-1234</p></td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>The ID of the parameter in the external system. </p><p>Example: MPNID</p></td></tr><tr><td>type</td><td><code>string</code></td><td><p>The type of the parameter definition. </p><p>Example: SingleLineText</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The display name of the parameter. </p><p>Example: Microsoft Partner Network ID</p></td></tr><tr><td>value</td><td><code>string</code></td><td><p>The value of the parameter. </p><p>Example: 65272478BB01A12</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="CERTIFICATE OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "CER-1234-5678-9012",
  "href": "/v1/program/certificates/CER-1234-5678-9012",
  "program": {
    "id": "PRG-1234-5678",
    "href": "/program/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner"
  },
  "certificant": {
    "id": "ACC-1234-1222",
    "href": "/accounts/accounts/ACC-1234-1222",
    "name": "Oscorp Industries",
    "icon": "/static/ACC-1234-1222/account.png"
  },
  "status": "Active",
  "parameters": {
    "fulfillment": [
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
    ],
    "ordering": [
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
  }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

