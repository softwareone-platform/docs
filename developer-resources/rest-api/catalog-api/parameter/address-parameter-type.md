# Address Parameter Type

The “Address” type parameter is one of the components that produces object type output value. It also provides some out-of-the-box validation, such as all fields are mandatory, contributing to elaborate data collection. The value type is `object`.

<table><thead><tr><th width="173">Field</th><th width="137">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>Label of the widget. </p><p>Example: Buyer address</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Define buyer address</p></td></tr><tr><td>defaultValue</td><td><p>One of:</p><p><code>None</code></p><p><code>Buyer</code></p><p><code>Seller</code></p><p><code>Licensee</code></p></td><td><p>(optional) Default value. </p><p>Example: Buyer</p></td></tr></tbody></table>

### Options Example <a href="#options-example" id="options-example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Seller address",
  "hintText": "Provide seller address",
  "defaultValue": "Seller"
}
```
{% endcode %}

### Value Fields <a href="#value-fields" id="value-fields"></a>

<table><thead><tr><th width="167">Field</th><th width="124">Type</th><th>Description</th></tr></thead><tbody><tr><td>addressLine1</td><td>string</td><td>Address Line1 - street address. Example: 123 Main Street</td></tr><tr><td>addressLine1</td><td>string</td><td>Address Line 2 - door number. Example: Apt 4B</td></tr><tr><td>postCode</td><td>string</td><td><p>Post or ZIP code.</p><p>Example: 12345</p></td></tr><tr><td>city</td><td>string</td><td><p>City or town name.</p><p>Example: Cityville</p></td></tr><tr><td>state</td><td>string</td><td><p>State name or abbreviation. </p><p>Example: S</p></td></tr><tr><td>country</td><td>string</td><td><p>Country code according to standard. </p><p>Example: ST</p></td></tr></tbody></table>

### Value Example <a href="#value-example" id="value-example"></a>

{% code lineNumbers="true" %}
```json
{
  "addressLine1": "123 Main Street",
  "addressLine2": "Apt 4B",
  "postCode": "12345",
  "city": "Cityville",
  "state": "S",
  "country": "ST"
}
```
{% endcode %}
