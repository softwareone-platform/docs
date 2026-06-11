# Address

The `address` object indicates a postal address. It contains the following fields:

<table><thead><tr><th width="147">Field Name</th><th width="126">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>addressLine1</code></td><td>string</td><td>The line 1 of the postal address.</td></tr><tr><td><code>addressLine2</code></td><td>string</td><td>The line 2 of the postal address.</td></tr><tr><td><code>postCode</code></td><td>string</td><td>The post code or ZIP code for the address.</td></tr><tr><td><code>city</code></td><td>string</td><td>The city or town name for the address.</td></tr><tr><td><code>state</code></td><td>string</td><td>The full name or abbreviation for the state. </td></tr><tr><td><code>country</code></td><td>string</td><td>The country code in the <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes">ISO </a>format. </td></tr></tbody></table>

### Example

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
