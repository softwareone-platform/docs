# Category

The Category Object enables the operator to add, view delete category object.

<table><thead><tr><th width="169">Field Name</th><th width="116">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The ID of the category object. </p><p>Example: EXC-0001</p></td></tr><tr><td><code>name</code></td><td>string</td><td><p>The name of the category object. </p><p>Example: Automotive</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>The description of the category object. </p><p>Example: Build a solid foundation with the support of workplace specialists who take the time to understand your unique business needs.</p></td></tr><tr><td><code>status</code></td><td>enum</td><td>Indicates the status of the category. Allowed values:  <code>active</code> or <code>disabled</code>.</td></tr><tr><td><code>revision</code></td><td>integer</td><td><p>The revision number of the category. </p><p>Example: 1</p></td></tr><tr><td><code>audit</code></td><td>object</td><td> A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

### Example response <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
 {
    "id": "EXC-0001",
    "name": "Automotive",
    "revision": 1,
    "description": "Build a solid foundation with the support of workplace specialists who take the time to understand your unique business needs.",
    "status": "Active",
    "audit": {
     "created": { "at": "...", "by": { } },
     "updated": { "at": "...", "by": { } }
   }
 }
```
{% endcode %}
