# Instance

<table><thead><tr><th width="149">Field Name</th><th width="168">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>Primary instance identifier.</p><p>Example: INS-1234-1234-0001</p></td></tr><tr><td><code>extension</code></td><td><a href="../extension/">extension</a></td><td>The related <a href="../extension/"><code>extension</code></a>. </td></tr><tr><td><code>version</code></td><td>string</td><td><p>The version of the extension code this instance is running as provided by the instance itself. </p><p>Example: version123</p></td></tr><tr><td><code>meta</code></td><td>extensionMeta</td><td>Extension metadata of the instance. </td></tr><tr><td><code>channel</code></td><td>object</td><td>A reference to the <a href="./#channel-object"><code>channel</code></a> object. </td></tr><tr><td><code>status</code></td><td>string</td><td>The status of the extension instance. Allowed values:  <code>connecting</code>, <code>running</code>, <code>disconnected</code>, or <code>deleted</code>.</td></tr><tr><td><code>externalId</code></td><td>string</td><td>Identifier of the currently running instance. It must be logically unique for a given Extension (excluding Deleted instances).</td></tr><tr><td><code>audit</code></td><td>object</td><td> A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Channel object <a href="#channel-object" id="channel-object"></a>

<table><thead><tr><th width="151">Field</th><th width="207">Type</th><th>Description</th></tr></thead><tbody><tr><td>identity</td><td>object</td><td>Ziti identity</td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
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
