# Extension

The Extension object represents a set of requirements (parameters) that vendors ask their clients to meet. Think of it as a checklist (extension parameters) that ensures clients are ready and able to work with the vendor’s products or services.

<table><thead><tr><th width="191">Field Name</th><th width="186">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The identifier for the extension. </p><p>Example: EXT-1234-5678</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the extension. </p><p>Example: Microsoft AI Cloud Partner</p></td></tr><tr><td><code>website</code></td><td>URI</td><td><p>The URL for the extension website. </p><p>Example: Microsoft AI Cloud Partner</p></td></tr><tr><td><code>icon</code></td><td>string</td><td><p>The logo of the extension. </p><p>Example: /v1/extension/extensions/EXT-1234-1234/icon</p></td></tr><tr><td><code>shortDescription</code></td><td>string</td><td><p>A short description of the extension.</p><p>Example: Microsoft 365 and Office 365 are cloud-based productivity suites</p></td></tr><tr><td><code>longDescription</code></td><td>string</td><td><p>A long description of the extension. </p><p>Example: Microsoft 365 and Office 365 are cloud-based productivity suites that offer a range of applications and services to help businesses of all sizes work more efficiently.</p></td></tr><tr><td><code>categories</code></td><td>object (<a href="../category/"><code>category</code></a>)</td><td><p>Contains a list of selected categories. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[ 
    { 
        "id": "EXC-1111-1111", 
        "name": "Accounting &#x26; finance"  
    } 
]
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/account/">account</a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[ 
    { 
        "id": "EXC-1111-1111", 
        "name": "Accounting &#x26; finance"  
    } 
]
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td><p>The status of the extension. Possible values are </p><ul><li><code>Draft</code></li><li><code>Deleted</code>  - Can be deleted if it's in a draft state.</li><li><code>Public</code> - Available in the extensions directory. Only an Operations user can make the extension public.</li><li><code>Private</code> - Not available in the extensions directory, but can be accessed through an invitation.</li></ul></td></tr><tr><td><code>statistics</code></td><td>object</td><td><p>A reference to the <a href="./#extensionstatistics"><code>extensionStatistics</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
<strong>  "installations": 100
</strong>}
</code></pre></td></tr><tr><td><code>configuration</code></td><td>object</td><td><p>Configuration object. Available only if retrieved with the extension’s token or vendor token. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "adobe_secret": "***",
   "mpt_token": "***",
   "vendor": "ACC-123-123"
}
</code></pre></td></tr><tr><td><code>service</code></td><td>object</td><td><p><a href="./#service">service</a> information. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "secret": "Fjh;fd93i4=[fjkjmk["
}
</code></pre></td></tr><tr><td><code>meta</code></td><td>object</td><td><p>A reference to the <code>extensionMeta</code> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ "id": "EXM-1234-1234" }
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td> A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Extension Statistics object <a href="#extensionstatistics" id="extensionstatistics"></a>

<table><thead><tr><th width="158">Field Name</th><th width="193">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>installations</code></td><td>integer</td><td><p>The number of installations assigned to the extension. </p><p>Example: 100</p></td></tr></tbody></table>

### Service object <a href="#service" id="service"></a>

<table><thead><tr><th width="154">Field Name</th><th width="202">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>secret</code></td><td>string</td><td><p>Represents the secret key. </p><p>Example: <code>ds340ffdjBfdj9834hfin4g</code></p></td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
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
