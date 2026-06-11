# Category

The Category Object enables the operator to add, view, or delete a category object.

<table><thead><tr><th width="169">Field</th><th width="116">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The ID of the category object. </td></tr><tr><td><code>name</code></td><td>string</td><td>Name of the category object. </td></tr><tr><td><code>description</code></td><td>string</td><td>A description of the category object. </td></tr><tr><td><code>status</code></td><td>enum</td><td>Indicates the status of the category. Allowed values are  <code>active</code> or <code>disabled</code>.</td></tr><tr><td><code>revision</code></td><td>integer</td><td>The revision number of the category. </td></tr><tr><td><code>audit</code></td><td>object</td><td> Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Example <a href="#example" id="example"></a>

{% code title="CATEGORY OBJECT" overflow="wrap" lineNumbers="true" %}
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
