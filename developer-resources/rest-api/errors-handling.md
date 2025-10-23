# Error Handling

All errors reported by the [REST API](./) have an [HTTP status code](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) and follow the standard format.&#x20;

When an error occurs, the response body usually contains a JSON object with the following fields:

{% code lineNumbers="true" %}
```json
{
  "type": "https://tools.ietf.org/html/rfc9110#section-15.5.1",
  "title": "Bad Request",
  "status": 400,
  "detail": "One or more validation errors occurred.",
  "traceId": "00-9e02a91b64ac56904703a3a69ea9101d-56be90a29d0b0b25-00",
  "errors": {
    "mistake": [
      "Unknown expression group."
    ]
  }
}
```
{% endcode %}

* **type** - \[string] A URI reference that identifies the error type, providing a consistent way to categorize errors across different API implementations.
* **title** - \[string] A human-readable title or summary of the error.
* **status** - \[number] The HTTP status code associated with the error.
* **detail** - (Optional) \[string] A detailed human-readable description of the error, providing additional information to help clients understand the issue.
* **instance** - (Optional) \[string] A URI reference that identifies the specific occurrence of the error, useful for debugging or tracing purposes.
* **traceId** - (Optional) \[string] A unique identifier to trace requests in logs.
* **errors** - (Optional) \[key-value] A collection of errors detected by validation logic.

## Common errors

The following table lists some of the common errors:

<table><thead><tr><th width="245">HTTP status</th><th>Description</th></tr></thead><tbody><tr><td><strong>401</strong> Unauthorized</td><td>This means the request lacks valid authentication credentials for the target resource. Check if the Authorization header is present and contains the valid token value.</td></tr><tr><td><strong>403</strong> Forbidden</td><td>The server understands the request but refuses to authorize it.</td></tr><tr><td><strong>404</strong> Not Found</td><td>The requested resource could not be found on the server.</td></tr><tr><td><strong>409</strong> Conflict</td><td>The request could not be completed due to a conflict with the current state of the resource.</td></tr><tr><td><strong>415</strong> Unsupported Media Type</td><td>The server refuses the request because the payload format is not supported.</td></tr><tr><td><strong>500</strong> Internal Server Error</td><td>The server encountered an unexpected condition that prevented it from fulfilling the request.</td></tr><tr><td><strong>501</strong> Not Implemented</td><td>The server does not support the functionality required to fulfill the request.</td></tr><tr><td><strong>504</strong> Gateway Timeout</td><td>The server, while acting as a gateway or proxy, did not receive a timely response from an upstream server.</td></tr></tbody></table>
