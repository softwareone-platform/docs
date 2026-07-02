# Extension

The Extension object represents a set of requirements (parameters) that vendors ask their clients to meet. Think of it as a checklist (extension parameters) that ensures clients are ready and able to work with the vendor’s products or services.

<table data-search="false"><thead><tr><th width="191">Field</th><th width="151">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The identifier for the extension. </td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the extension. </td></tr><tr><td><code>website</code></td><td>URI</td><td>(Optional) URL for the extension website.</td></tr><tr><td><code>icon</code></td><td>string, core</td><td>The logo of the extension. </td></tr><tr><td><code>shortDescription</code></td><td>string</td><td>(Optional) A short description of the extension.</td></tr><tr><td><code>longDescription</code></td><td>string</td><td>(Optional) A long description of the extension. </td></tr><tr><td><code>categories</code></td><td>object</td><td>Represents the <a href="../category/"><code>category</code></a> object, which contains a list of selected categories. </td></tr><tr><td><code>vendor</code></td><td>object</td><td>Represents the vendor <a href="../../accounts-api/account/"><code>account</code></a> object. </td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The status of the extension. Allowed values are: </p><ul><li><code>Draft</code></li><li><code>Deleted</code>  - Can be deleted if it's in a draft state.</li><li><code>Public</code> - Available in the extensions directory. Only an Operations user can make the extension public.</li><li><code>Private</code> - Not available in the extensions directory, but can be accessed through an invitation.</li></ul></td></tr><tr><td><code>statistics</code></td><td>object</td><td>(Read-only) Represents the <a href="./#extensionstatistics"><code>extensionStatistics</code></a> object. </td></tr><tr><td><code>configuration</code></td><td>object</td><td>Represents the <code>configuration</code> object. Available only if retrieved with the extension’s token or vendor token.</td></tr><tr><td><code>service</code></td><td>object</td><td>Represents the <a href="./#service"><code>service</code></a> object. </td></tr><tr><td><code>meta</code></td><td>object</td><td>(Read-only) (Optional) Represents the <code>extensionMeta</code> object.</td></tr><tr><td><code>audit</code></td><td>object</td><td> Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Extension Statistics object <a href="#extensionstatistics" id="extensionstatistics"></a>

<table><thead><tr><th width="158">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>installations</code></td><td>integer</td><td>(Read-only) Number of installations assigned to the extension. </td></tr></tbody></table>

## Service object <a href="#service" id="service"></a>

<table><thead><tr><th width="154">Field</th><th width="154">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>secret</code></td><td>string</td><td>Represents the secret key. </td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="EXTENSION OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
  "id": "EXT-1234-5678",
  "name": "Microsoft AI Cloud Partner extension",
  "website": "https://www.microsoft.com",
  "icon": "/v1/extension/extensions/EXT-1234-1234/icon",
  "shortDescription": "Microsoft 365 and Office 365 extension",
  "longDescription": "Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently.",
   "categories": [
      { 
          "id": "EXC-1111-1111", 
          "name": "Accounting & finance"
      } 
  ],
  "vendor": {
      "id": "ACC-1234-1234"
  },
  "status": "Private",
  "statistics": {
    "installations": 100
  },
  "service": {
    "secret": "ds340ffdjBfdj9834hfin4g"
  }
  "configuration": {
    "prop1": "value"
  },
  "meta": {
    "id": "EXM-1234-1234"
  }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
