# Installation

<table><thead><tr><th width="143">Field Name</th><th width="158">Data Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>The identifier for the primary installation. </p><p>Example: EXI-1234-1234-0001</p></td></tr><tr><td>extension</td><td>object</td><td>The <a href="../extension/"><code>extension</code></a> to which the installation item belongs. </td></tr><tr><td>status</td><td>enum</td><td>The status of the installation. Allowed values:  <code>installed</code>, <code>uninstalled</code>, <code>invited</code>, or <code>expired</code>.</td></tr><tr><td>configuration</td><td><code>JsonColumn</code> (encrypted)</td><td><p>A set of key values parameters required for extension. Some values can be sensitive, so those must be hidden. This field is available only if retrieved with the extension’s token or vendor token. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
   "adobe_secret": "***",
   "mpt_token": "***",
   "vendor": "ACC-123-123"
}
</code></pre></td></tr><tr><td>account</td><td>object</td><td><p>A reference to the vendor account object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
<strong>    "id": "ACC-1234-1234",   
</strong>    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>invitation</td><td>object</td><td><p><a href="../invitation.md">invitation</a> information. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "url": "https://client.softwareone.com/accept-invite?code=invitationCode",
  "status": "Invited"
}
</code></pre></td></tr><tr><td>modules</td><td>object</td><td><p>The list of modules the user gave consent to. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
 {
   "id": "MOD-123"
 },
 {
   "id": "MOD-433"
 }
]
</code></pre></td></tr><tr><td>audit</td><td>object</td><td> A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
  {
    "id": "EXI-1234-1234-0001",
    "extension": {
      "id": "EXT-6822-9898-4256",
      "name": "Microsoft AI Cloud Partner"
    },
    "status": "Installed",
    "configuration": {
      "adobe_secret": "***",
      "mpt_token": "***",
      "vendor": "ACC-123-123"
    },
    "account": {
      "id": "ACC-1234-1234"
    },
    "invitation": {
        "code": "TEST",
        "status": "Invited"
    }
    "audit": {
      "created": { "at": "...", "by": { } },
      "updated": { "at": "...", "by": { } }
   }
 }
```
{% endcode %}
