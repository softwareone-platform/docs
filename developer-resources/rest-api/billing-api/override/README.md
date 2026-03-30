# Override

The Override object marks the clients as eligible for manual billing, bypassing automated billing.&#x20;

Assigning this object indicates that the client's billing requires flexibility and will be handled manually.&#x20;Only SoftwareOne Operations can see overrides.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="134">Field Name</th><th width="148">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>The unique identifier for the object. No nesting exists for this identifier. </p><p>Example: BOV-1234-1239</p></td></tr><tr><td><code>client</code></td><td>object</td><td><p>A reference to the client <a href="../../accounts-api/account/"><code>account</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-4444",
    "href": "/accounts/accounts/ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td><code>vendor</code></td><td>object</td><td><p>A reference to the vendor <a href="../../accounts-api/account/"><code>account</code></a> object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum</td><td>The status of the override. Allowed values: <code>active</code> or <code>disabled</code>. </td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The external identifier or reference number. This value is optional.</p><p>Example: bill-12345609</p></td></tr><tr><td><code>notes</code></td><td>string</td><td><p>Notes associated with the override.</p><p>Example: Based on the reporting figures, we decided to move this client to manual billing.</p></td></tr><tr><td><code>audit</code></td><td>object</td><td><p>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object. Allowed values:  <code>created</code> or <code>updated</code>. </p><p>Example:</p><pre class="language-json" data-line-numbers><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

