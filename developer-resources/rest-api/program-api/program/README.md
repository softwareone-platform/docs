# Program

The Program object represents a set of requirements (parameters) that vendors ask their clients to meet.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="170">Field</th><th width="166">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The program's identifier. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The program name. </td></tr><tr><td><code>website</code></td><td>string</td><td>The URL of the program website. </td></tr><tr><td><code>icon</code></td><td>string, core</td><td>The program logo or icon.</td></tr><tr><td><code>shortDescription</code></td><td>string</td><td>(Optional) A short description of program, shown in the card.</td></tr><tr><td><code>longDescription</code></td><td>string</td><td>(Optional) A long description of program, shown on details page.</td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>The status of the program. Allowed values are</p><ul><li><code>None</code></li><li><code>Draft</code></li><li><code>Published</code></li><li><code>Unpublished</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>eligibility</code></td><td>string, core</td><td>Represents an object for storing information for the clients and reseller flags.</td></tr><tr><td><code>applicableTo</code></td><td>string, core</td><td>Allowed values are  <code>buyer</code> or <code>licensee</code>.</td></tr><tr><td><code>products</code></td><td>object, core</td><td><p>Represents the <a href="../../catalog-api/product/"><code>product</code></a> object, containing a list of selected products. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[ 
    { 
        "id": "PRD-1111-1111", 
        "name": "Microsoft Office 365 NCE", 
        "externalIds": {},
        "icon": "/static/PRD-1111-1111-1111/logo.png",
        "status": "Published" 
    } 
]
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object. Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "type": "Vendor",
    "status": "Enabled",
    "name": "Microsoft"
}
</code></pre></td></tr><tr><td><code>settings</code></td><td>object</td><td><p>Represents the <a href="./#programsettings"><code>programSettings</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">	"settings": {
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
</code></pre></td></tr><tr><td><code>statistics</code></td><td>object</td><td><p>(Read-only) Represents the <a href="./#programstatistics"><code>programStatistics</code></a> object. Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "certificates": 110
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Program Settings object <a href="#programsettings" id="programsettings"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="297.888916015625">Field</th><th width="105.4444580078125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>newCertificateAutoapprove</code></td><td>boolean</td><td>Automatically activates every new certificate request for this program.</td></tr><tr><td><code>programEnrolment</code></td><td>boolean</td><td>Displays the <strong>Enrol</strong> button on the program profile, enabling the client to place a request for this program. </td></tr><tr><td><code>programLink</code></td><td>boolean</td><td>Displays the <strong>Info</strong> button on the program profile, enabling clients to go to a URL to get more information. </td></tr><tr><td><code>terminateOnExpiration</code></td><td> boolean</td><td>Terminates the certificate on the expiration date, if the certificates have an expiration date.</td></tr><tr><td><code>terminateOnExpiration.enabled</code></td><td>boolean</td><td>Sets whether the certificates expire. </td></tr><tr><td><code>terminateOnExpiration.duration</code></td><td>number</td><td>The duration in days. </td></tr><tr><td><code>preValidation</code></td><td> boolean</td><td>Contains settings for the prevalidation phase during enrollment.</td></tr><tr><td><code>preValidation.enrollmentDraft</code></td><td>boolean</td><td>Validates change enrollment during the creation and before the enrollment is submitted. </td></tr><tr><td><code>preValidation.enrollmentQuerying</code></td><td>boolean</td><td>Validates querying enrollment during the creation and before the enrollment is submitted.</td></tr><tr><td><code>preValidation.reEnrollment</code></td><td>boolean</td><td>Validates before and during the re-enrollment. </td></tr></tbody></table>

## Program Statistics object <a href="#programstatistics" id="programstatistics"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="179">Field</th><th width="135">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>certificates</code></td><td>integer</td><td>(Read-only) Total number of verified certificates. </td></tr></tbody></table>

## Example

{% code title="PROGRAM OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
