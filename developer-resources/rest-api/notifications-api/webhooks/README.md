# Webhooks API

## Webhook object <a href="#title-text" id="title-text"></a>

<table><thead><tr><th width="190">Field</th><th width="144">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>string</td><td><p>Primary webhook identifier. </p><p></p><p>Example: <code>WBH-5433-8787</code></p></td></tr><tr><td>href</td><td>string</td><td>Relative reference to object on API (always <code>/notifications/webhooks/{id}</code>)</td></tr><tr><td>description</td><td>string</td><td><p>Description of the webhook. </p><p></p><p>Example: Webhook for Purchase Order Draft validation for Product Microsoft Office 36</p></td></tr><tr><td>status</td><td>enum</td><td><p>Status of a webhook.  </p><p></p><p>Example: Enabled</p></td></tr><tr><td>type</td><td>enum</td><td><p>Defines what for webhook is designed for. </p><p></p><p>Example: ValidatePurchaseOrderDraft</p></td></tr><tr><td>objectType</td><td>enum</td><td><p>Object that triggers webhook event. </p><p></p><p>Example: Order</p></td></tr><tr><td>url</td><td>string</td><td><p>Only https:// endpoints are allowed. </p><p></p><p>Example: https://some-api.vendor.com/order-validation</p></td></tr><tr><td>criteria</td><td>object</td><td>List of key value objects necessary to be present and of given value inside the payload of an webhook for webhook call to be triggered.</td></tr><tr><td>statistics</td><td>Statistics</td><td><p>Statistical and debug information regarding webhook executions. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
  "total": 1234,
  "successes": 1132,
  "failures": 101,
  "failuresSinceLastSuccess": 2
}
</code></pre></td></tr><tr><td>lastSuccess</td><td>Call</td><td><p>Last successful call to webhook URL. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json"><strong>{
</strong>  "succcess": true,
  "callTime": "2024-12-12T11:11:11",
  "responseTime": "2024-12-12T11:12:03",
  "httpStatusCode": "200",
  "reasonPhrase": "OK",
  "headers": {
    "Date": "Wed, 15 May 2024 10:16:56 GMT",
  },
  "error": null,
  "response": { ... }
}
</code></pre></td></tr><tr><td>lastFailure</td><td>Call</td><td><p>Last failed call to webhook URL. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">  {
  "succcess": true,
  "callTime": "2024-12-12T11:11:11",
  "responseTime": "2024-12-12T11:12:03",
  "status": "401",
  "reasonPhrase": "Auth Error",
  "response": "Unauthenticated",
  "headers": {
    "Date": "Wed, 15 May 2024 10:16:56 GMT",
  },
  "error": "JWT Token was invalid",
  "response": null,
}
</code></pre></td></tr><tr><td>lastCall</td><td>Call</td><td><p>Last call to webhook URL. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">  {
  "succcess": true,
  "callTime": "2024-12-12T11:11:11",
  "responseTime": "2024-12-12T11:12:03",
  "httpStatusCode": "200",
  "reasonPhrase": "OK",
  "headers": {
    "Date": "Wed, 15 May 2024 10:16:56 GMT",
  },
  "error": null,
  "response": { ... }
}
</code></pre></td></tr><tr><td>secret</td><td>string</td><td><p>Secret used for authorization purposes in 3rd party systems.</p><p>Only returned one time in response to Create Webhook Endpoint. </p><p></p><p>Example: 3ct^6NoryQN22V</p></td></tr><tr><td>account</td><td>Ref&#x3C;Account></td><td><p>Reference to vendor Account object<br>filled in on creation according to the current user account. </p><p></p><p>Example: </p><pre class="language-json"><code class="lang-json">{
  "id": "ACC-1234-1234",
  "href": "/accounts/accounts/ACC-1234-1234",
  "name": "Microsoft",
  "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>audit</td><td>AuditObject</td><td><p>Audit object with possible entries: created, updated, enabled, disabled according to life-cycle of the object. Example: </p><pre class="language-json"><code class="lang-json"> {
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } },
  "enabled": { "at": "...", "by": { } },
  "disabled": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

## Statistics <a href="#statistics" id="statistics"></a>

<table><thead><tr><th width="245">Field</th><th width="178">Type</th><th>Description</th></tr></thead><tbody><tr><td>total</td><td>number</td><td><p>Total number of calls made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  77</p></td></tr><tr><td>successes</td><td>number</td><td><p>Total successful number of calls made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  70</p></td></tr><tr><td>failures</td><td>number</td><td><p>Total failed number of calls that were made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  7</p></td></tr><tr><td>failuresSinceLastSuccess</td><td>number</td><td><p>Failed number of calls since last successful call that was made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  3</p></td></tr></tbody></table>

## Call <a href="#call" id="call"></a>

<table><thead><tr><th width="245">Field</th><th width="178">Type</th><th>Description</th></tr></thead><tbody><tr><td>total</td><td>number</td><td><p>Total number of calls made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  77</p></td></tr><tr><td>successes</td><td>number</td><td><p>Total successful number of calls made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  70</p></td></tr><tr><td>failures</td><td>number</td><td><p>Total failed number of calls that were made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  7</p></td></tr><tr><td>failuresSinceLastSuccess</td><td>number</td><td><p>Failed number of calls since last successful call that was made from MPT to an external system represented by the Webhook Object. </p><p></p><p>Example:  3</p></td></tr></tbody></table>

## Example

{% tabs %}
{% tab title="Webhook Object" %}
```json
{
  "id": "WBH-5433-8787",
  "href": "/notifications/webhooks/WBH-5433-8787",
  "description": "Webhook for some products"
  "account": {
    "id": "ACC-7362-0233",
    "href": "/accounts/accounts/ACC-7362-0233",
    "name": "Adobe",
    "icon": "/static/ACC-7362-0233/account.png"
  },
  "objectType": "order",
  "type": "validatePurchaseOrderDraft",
  "params": {
    "product.id": "PRD-6233-9657"
  },
  "status": "enabled",
  "url": "https://my-webhook.endpoint.com/validation",
  "secret": "*******************",
  "statistics": {
    "total": 1234,
    "successes": 1132,
    "failures": 101,
    "failuresSinceLastSuccess": 2
  },
  "lastSuccess": {
    "succcess": true,
    "callTime": "2024-12-12T11:11:11",
    "responseTime": "2024-12-12T11:12:03",
    "httpStatusCode": "200",
    "reasonPhrase": "OK",
    "headers": {
      "Date": "Wed, 15 May 2024 10:16:56 GMT",
    },
    "error": null,
    "response": { ... }
  },
  "lastFailure": {
    "succcess": true,
    "callTime": "2024-12-12T11:11:11",
    "responseTime": "2024-12-12T11:12:03",
    "status": "401",
    "reasonPhrase": "Auth Error",
    "response": "Unauthenticated",
    "headers": {
      "Date": "Wed, 15 May 2024 10:16:56 GMT",
    },
    "error": "JWT Token was invalid",
    "response": null,
  },
  "lastCall": {
    "succcess": true,
    "callTime": "2024-12-12T11:11:11",
    "responseTime": "2024-12-12T11:12:03",
    "httpStatusCode": "200",
    "reasonPhrase": "OK",
    "headers": {
      "Date": "Wed, 15 May 2024 10:16:56 GMT",
    },
    "error": null,
    "response": { ... }
  },
  "audit": {
    "created": { "at": "...", "by": { } },
    "updated": { "at": "...", "by": { } }
  },
}
```
{% endtab %}
{% endtabs %}

