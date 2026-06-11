# Instance

<table><thead><tr><th width="149">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>(Read-only) The primary identifier for the instance.</td></tr><tr><td><code>extension</code></td><td>object</td><td>(Read-only) Represents the related <a href="../extension/"><code>extension</code></a>. </td></tr><tr><td><code>version</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>Represents the version of the extension code that this instance is running, as reported by the instance itself.</td></tr><tr><td><code>meta</code></td><td>object</td><td>Represents the <code>extensionMeta</code> object which contains the extension metadata of the instance. </td></tr><tr><td><code>channel</code></td><td>object</td><td>(Read-only) Represents the <a href="./#channel-object"><code>channel</code></a> object. </td></tr><tr><td><code>status</code></td><td>string, core</td><td><p>The status of the extension instance. Allowed values are: </p><ul><li><code>Connecting</code></li><li><code>Running</code></li><li><code>Disconnected</code></li><li><code>Deleted</code></li></ul></td></tr><tr><td><code>externalId</code></td><td>string</td><td>(Read-only) Identifier of the currently running instance. It must be logically unique for a given Extension (excluding Deleted instances).</td></tr><tr><td><code>audit</code></td><td>object</td><td> Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Channel object <a href="#channel-object" id="channel-object"></a>

<table><thead><tr><th width="151">Field</th><th width="193">Type</th><th>Description</th></tr></thead><tbody><tr><td>identity</td><td>object</td><td>(Read‑only) Represents the Ziti identity.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="INSTANCE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
 {
    "id": "INS-1234-1234-0001",
    "extension": {
      "id": "EXT-6822-9898-4256",
      "href": "/extensions/EXT-6822-9898-4256",
      "name": "Microsoft AI Cloud Partner"
    },
    "status": "Running",
    "meta": {..},
    "channel": { }
    "externalId": "f81d4fae-7dec-11d0-a765-00a0c91e6bf6",
    "audit": {
      "created": { "at": "...", "by": { } },
      "updated": { "at": "...", "by": { } }
   }
 }
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
