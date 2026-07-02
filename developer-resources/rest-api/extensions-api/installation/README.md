# Installation

The Installation Object allows you to add, view, and delete installation objects.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-search="false"><thead><tr><th width="162">Field</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td>(Read-only) The identifier for the primary installation. </td></tr><tr><td>extension</td><td>object</td><td>(Read-only) The <a href="../extension/"><code>extension</code></a> to which the installation item belongs. </td></tr><tr><td>status</td><td>enum, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td><p>The status of the installation. Allowed values are:</p><ul><li><code>Installed</code></li><li><code>Uninstalled</code></li><li><code>Invited</code></li><li><code>Expired</code></li></ul></td></tr><tr><td>configuration</td><td><code>JsonColumn</code> (encrypted)</td><td>(Read‑only) A set of key–value parameters required by the extension. Some values may be sensitive and must be hidden. This field is available only when retrieved using the extension’s token or a vendor token.</td></tr><tr><td>account</td><td>object</td><td>Represents the vendor account object. </td></tr><tr><td>invitation</td><td>object</td><td>(Read-only) Represents the <a href="invitation-object.md"><code>invitation</code></a> object, which contains the invitation information. </td></tr><tr><td>modules</td><td>object</td><td>Represents the list of modules the user has given consent to.</td></tr><tr><td>audit</td><td>object</td><td> Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="INSTALLATION OBJECT" overflow="wrap" lineNumbers="true" %}
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

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
