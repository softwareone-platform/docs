# Program

The Program object represents a set of requirements (parameters) that vendors ask their clients to meet.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="140">Field Name</th><th width="172">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The program's identifier. </p><p>Example: PRG-1234-5678</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the program.  </p><p>Example: Microsoft AI Cloud Partner</p></td></tr><tr><td><code>website</code></td><td>string</td><td><p>The URL for the program website. </p><p>Example: https://www.microsoft.com</p></td></tr><tr><td><code>icon</code></td><td>string</td><td>The program logo's or icon.</td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the program. Allowed values:  <code>none</code>, <code>draft</code>, <code>published</code>, <code>unpublished</code>, or <code>deleted</code>.</td></tr><tr><td><code>eligibility</code></td><td>string</td><td>Represents an object for storing information for the clients and reseller flags.</td></tr><tr><td><code>applicableTo</code></td><td>string</td><td>Allowed values: <code>buyer</code> or <code>licensee</code>.</td></tr><tr><td><code>products</code></td><td>object (<a href="../../catalog-api/product/"><code>produc</code>t</a>)</td><td><p>Contains a list of selected products. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[ 
    { 
        "id": "PRD-1111-1111", 
        "name": "Microsoft Office 365 NCE", 
        "externalIds": {},
        "icon": "/static/PRD-1111-1111-1111/logo.png",
        "status": "Published" 
    } 
]
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/account/"><code>account</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "type": "Vendor",
    "status": "Enabled",
    "name": "Microsoft"
}
</code></pre></td></tr><tr><td><code>settings</code></td><td>object (<a href="./#programsettings"><code>programSettings</code></a>)</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">"settings": {
        "newCertificateAutoapprove": true,
        "programEnrollment": false,
        "programLink": false,
        "terminateOnExpiration": {
            "enabled": true,
            "duration": 30
        },
        "preValidation": {
            "enrollmentDraft": false,
            "enrollmentQuerying": false,
            "reEnrollment": false
        }
} 
</code></pre></td></tr><tr><td><code>statistics</code></td><td>object (<a href="./#programstatistics"><code>programStatistics</code></a>)</td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "certificates": 110
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## ProgramSettings object <a href="#programsettings" id="programsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="280.888916015625">Field Name</th><th width="139">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>newCertificateAutoapprove</code></td><td>boolean</td><td>Automatically activates every new certificate request for this program. Example: true</td></tr><tr><td><code>programEnrolment</code></td><td>boolean</td><td><p>Displays the <strong>Enrol</strong> button on the program profile, enabling the client to place a request for this program. </p><p>Example: true</p></td></tr><tr><td><code>programLink</code></td><td>boolean</td><td><p>Displays the <strong>Info</strong> button on the program profile, enabling clients to go to a URL to get more information. </p><p>Example: true</p></td></tr><tr><td><code>terminateOnExpiration</code></td><td> boolean</td><td><p>Terminates the certificate on the expiration date, if the certificates have an expiration date.</p><p>Example: true</p></td></tr><tr><td><code>terminateOnExpiration.enabled</code></td><td>boolean</td><td><p>Sets whether the certificates expire. </p><p>Example: true</p></td></tr><tr><td><code>terminateOnExpiration.duration</code></td><td>number</td><td><p>The duration in days. </p><p>Example: 30</p></td></tr><tr><td><code>preValidation</code></td><td> boolean</td><td><p>Contains settings for the prevalidation phase during enrollment. </p><p>Example: true</p></td></tr><tr><td><code>preValidation.enrollmentDraft</code></td><td>boolean</td><td><p>Validates change enrollment during the creation and before the enrollment is submitted. </p><p>Example: false</p></td></tr><tr><td><code>preValidation.enrollmentQuerying</code></td><td>boolean</td><td><p>Validates querying enrollment during the creation and before the enrollment is submitted.</p><p>Example: false</p></td></tr><tr><td><code>preValidation.reEnrollment</code></td><td>boolean</td><td><p>Validates before and during the re-enrollment. </p><p>Example: false</p></td></tr></tbody></table>

## Program Statistics object <a href="#programstatistics" id="programstatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="272">Field Name</th><th width="172">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>certificates</code></td><td>integer</td><td><p>The total number of verified certificates. </p><p>Example: 1</p></td></tr></tbody></table>

## Example response

{% code lineNumbers="true" %}
```json
{
  "id": "PRG-1234-5678",
  "name": "Microsoft AI Cloud Partner",
  "website": "https://www.microsoft.com",
  "icon": "/v1/program/programs/PRG-1234-1234/icon",
  "status": "Draft",
  "eligibility": {
    "client": true,
    "partner": true
  },
  "applicableTo": "Buyer",
  "products": [
      { 
          "id": "PRD-1111-1111", 
          "name": "Microsoft Office 365 NCE", 
          "externalIds": {},
          "icon": "/static/PRD-1111-1111-1111/logo.png",
          "status": "Published" 
      } 
  ],
  "vendor": {
      "id": "ACC-1234-1234",
      "type": "Vendor",
      "status": "Enabled",
      "name": "Microsoft"
  },
  "settings": {
      "newCertificateAutoapprove": true,
      "programEnrollment": false,
      "programLink": false,
      "terminateOnExpiration": {
          "enabled": true,
          "duration": 30
      },
      "preValidation": {
          "enrollmentDraft": false,
          "enrollmentQuerying": false,
          "reEnrollment": false
      }
  }, 
  "statistics": {
    "certificates": 100,
  }
}
```
{% endcode %}
