# Error

The `Error` object represents an error response returned by the Marketplace API when it encounters a non-2xx HTTP response code. This object includes the following fields:

### Fields

<table><thead><tr><th width="140">Field</th><th width="130">Type</th><th>Description</th></tr></thead><tbody><tr><td>title</td><td><code>string</code></td><td>A short description of the problem.</td></tr><tr><td>type</td><td><code>string</code></td><td>A URI reference that identifies the error type (Problem Details / RFC 7807).</td></tr><tr><td>status</td><td><code>number</code></td><td>The HTTP status code returned by the server.</td></tr><tr><td>details</td><td><code>string</code></td><td>A detailed description of the error message.</td></tr><tr><td>traceId</td><td><code>string</code></td><td>Represents an identifier used to trace a request.</td></tr><tr><td>errors</td><td><code>object</code> </td><td>A detailed list of errors that can be connected to the request data.</td></tr></tbody></table>

### Examples

{% tabs %}
{% tab title="ERROR OBJECT (WITHOUT PARAMETERS)" %}
{% code lineNumbers="true" %}
```json
{
  "title": "Order update failed",
  "detail": "External ID is too long",
  "status": 400,
  "type": "https://docs.platform.softwareone.com/developer-resources/rest-api/errors/commerce#MPTCOM03-0078",
  "traceId": "00-00000000000000000000000000000000-000000000000000-00"
}
```
{% endcode %}
{% endtab %}

{% tab title="ERROR OBJECT (WITH PARAMETERS)" %}
{% code lineNumbers="true" %}
```json
 {
  "title": "Order update failed",
  "detail": "Value of listing does not correspond to a valid listing; External ID is too long",
  "status": 400,
  "type": "https://docs.platform.softwareone.com/developer-resources/rest-api/errors/billing#MPTBIL03-0078",
  "traceId": "00-00000000000000000000000000000000-000000000000000-00",
  "errors": [
    {
      "message": "Value of listing does not correspond to a valid listing",
      "properties": [ "listing.id" ]
    },
    {
      "message": "External ID is too long",
      "properties": [ "externalId" ]
    }
  ]
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

### Detailed Errors <a href="#detailed-errors" id="detailed-errors"></a>

#### Parameter Errors Fields <a href="#parameter-errors-fields" id="parameter-errors-fields"></a>

<table><thead><tr><th width="159">Field</th><th width="130">Type</th><th>Description</th></tr></thead><tbody><tr><td>message</td><td><code>string</code></td><td>The message text with markdown allowed.</td></tr><tr><td>properties</td><td><code>list&#x3C;string></code></td><td>List of object properties affected by the error. </td></tr><tr><td>id</td><td><code>string</code></td><td>Message identifier used for the localization process.</td></tr><tr><td>parameters</td><td><code>object</code></td><td>Parameters that can be used in a message with <code>{{name}}</code> a template.</td></tr></tbody></table>
