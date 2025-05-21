# Address

The Address object indicates a postal address. It contains the following attributes:

<table><thead><tr><th width="147">Field</th><th width="126">Type</th><th>Description</th></tr></thead><tbody><tr><td>addressLine1</td><td><code>string</code></td><td>The line 1 of the postal address.</td></tr><tr><td>addressLine2</td><td><code>string</code></td><td>The line 2 of the postal address.</td></tr><tr><td>postCode</td><td><code>string</code></td><td>The post code or ZIP code for the address.</td></tr><tr><td>city</td><td><code>string</code></td><td>The city or town name for the address.</td></tr><tr><td>state</td><td><code>string</code></td><td>The full name or abbreviation for the state. </td></tr><tr><td>country</td><td><code>string</code></td><td>The country code in the <a href="https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes">ISO </a>format. </td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="ADDRESS OBJECT" %}
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
{% endtab %}
{% endtabs %}
