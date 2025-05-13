# Program Parameter Groups

The Parameter Group Object represents a group of parameters. This object contains the following attributes:

<table><thead><tr><th width="181">Field</th><th width="155">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The platform generated ID. </p><p>Example: PGR-6790-8304-0001</p></td></tr><tr><td>href</td><td><code>string</code></td><td><p>Relative reference to the object in the API. </p><p>Example: /programs/PRG-6790-8304-0171/parameter-groups/PGR-6790-8304-0001</p></td></tr><tr><td>name</td><td><code>string</code></td><td><p>The name of the group. </p><p>Example: Parameters</p></td></tr><tr><td>label</td><td><code>string</code></td><td>Label displayed in the wizard steps selector. Example: Create agreement</td></tr><tr><td>description</td><td><code>string</code></td><td><p>Description of the group. </p><p>Example: When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.</p></td></tr><tr><td>displayOrder</td><td><code>integer</code></td><td><p>Defines the display order. </p><p>Example: 100</p></td></tr><tr><td>default</td><td><code>boolean</code></td><td><p>Marks the default item group. </p><p>Example: true</p></td></tr><tr><td>parameterCount</td><td><code>integer</code></td><td><p>The number of parameters in the group. </p><p>Example: 5</p></td></tr><tr><td>program</td><td><a href="../"><code>program</code></a></td><td>A reference to the Program object.</td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="PROGRAM PARAMETER GROUPS" %}
{% code overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "PGR-6790-8304-0001",
    "href": "/program/PRG-6790-8304/parameter-groups/PGR-6790-8304-0001",
    "title": "Parameters",
    "label": "Create agreement",
    "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
    "displayOrder": 100,
    "default": true,
    "program": {
        "id": "PRG-6790-8304-0171"
    }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}
