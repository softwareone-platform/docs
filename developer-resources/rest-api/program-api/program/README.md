# Program

## Program object

The Program object represents a set of requirements (parameters) that vendors ask their clients to meet. This object contains the following attributes:

<table><thead><tr><th width="140">Field</th><th width="172">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The program's identifier. </p><p>Example: PRG-1234-5678</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the program.  </p><p>Example: Microsoft AI Cloud Partner</p></td></tr><tr><td>website</td><td><code>string</code></td><td><p>The URL for the program website. </p><p>Example: https://www.microsoft.com</p></td></tr><tr><td>icon</td><td><code>string</code></td><td>The program logo's or icon.</td></tr><tr><td>status</td><td><code>string</code></td><td><p>The status of the program. </p><p>Possible values: <code>None</code>, <code>Draft</code>, <code>Published</code>, <code>Unpublished</code>, or <code>Deleted</code></p></td></tr><tr><td>eligibility</td><td><code>string</code></td><td>Represents an object for storing information for the clients and reseller flags.</td></tr><tr><td>applicableTo</td><td><code>string</code></td><td>Possible values: <code>Buyer</code> or <code>Licensee</code></td></tr><tr><td>products</td><td><a href="../../catalog-api/product/"><code>product</code></a></td><td><p>Contains a list of selected products. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">[ 
    { 
        "id": "PRD-1111-1111", 
        "name": "Microsoft Office 365 NCE", 
        "externalIds": {},
        "icon": "/static/PRD-1111-1111-1111/logo.png",
        "status": "Published" 
    } 
]
</code></pre></td></tr><tr><td>vendor</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the vendor Account object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "type": "Vendor",
    "status": "Enabled",
    "name": "Microsoft"
}
</code></pre></td></tr><tr><td>settings</td><td><a href="./#programsettings"><code>programSettings</code></a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">"settings": {
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
</code></pre></td></tr><tr><td>statistics</td><td><a href="./#programstatistics"><code>programStatistics</code></a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-full-width="true"><code class="lang-json">{
  "certificates": 110
}
</code></pre></td></tr><tr><td>audit</td><td><a href="../../common-api-objects/audit.md"><code>audit</code></a></td><td><p>The audit information object. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Program Settings object <a href="#programsettings" id="programsettings"></a>

<table><thead><tr><th width="272">Field</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td>newCertificateAutoapprove</td><td><code>boolean</code></td><td>Automatically activates every new certificate request for this program. Example: true</td></tr><tr><td>programEnrolment</td><td><code>boolean</code></td><td><p>Displays the <strong>Enrol</strong> button on the program profile, enabling the client to place a request for this program. </p><p>Example: true</p></td></tr><tr><td>programLink</td><td><code>boolean</code></td><td><p>Displays the <strong>Info</strong> button on the program profile, enabling clients to go to a URL to get more information. </p><p>Example: true</p></td></tr><tr><td>terminateOnExpiration</td><td> </td><td><p>Terminates the certificate on the expiration date, if the certificates have an expiration date.</p><p>Example: true</p></td></tr><tr><td>terminateOnExpiration.enabled</td><td><code>boolean</code></td><td><p>Sets whether the certificates expire. </p><p>Example: true</p></td></tr><tr><td>terminateOnExpiration.duration</td><td><code>number</code></td><td><p>The duration in days. </p><p>Example: 30</p></td></tr><tr><td>preValidation</td><td> </td><td><p>Contains settings for the pre-validation phase during enrollment. </p><p>Example: true</p></td></tr><tr><td>preValidation.enrollmentDraft</td><td><code>boolean</code></td><td><p>Validates change enrollment during the creation and before the enrollment is submitted. </p><p>Example: false</p></td></tr><tr><td>preValidation.enrollmentQuerying</td><td><code>boolean</code></td><td><p>Validates querying enrollment during the creation and before the enrollment is submitted.</p><p>Example: false</p></td></tr><tr><td>preValidation.reEnrollment</td><td><code>boolean</code></td><td><p>Validates before and during the re-enrollment. </p><p>Example: false</p></td></tr></tbody></table>

## Program Statistics object <a href="#programstatistics" id="programstatistics"></a>

<table><thead><tr><th width="272">Field</th><th width="172">Type</th><th>Description</th></tr></thead><tbody><tr><td>certificates</td><td><code>integer</code></td><td><p>The total number of verified certificates. </p><p>Example: 1</p></td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="PROGRAM OBJECT" %}
{% code overflow="wrap" lineNumbers="true" %}
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
{% endtab %}
{% endtabs %}
