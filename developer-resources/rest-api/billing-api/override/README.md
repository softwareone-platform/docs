# Override

The Override object marks the clients as eligible for manual billing, bypassing automated billing.&#x20;

Assigning this object indicates that the client's billing requires flexibility and will be handled manually.&#x20;Only SoftwareOne Operations can see overrides.

<table><thead><tr><th width="166">Field</th><th width="183">Type</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td><code>string</code></td><td><p>The unique identifier for the object. Note that no nesting exists for this identifier. </p><p>Example: BOV-1234-1239</p></td></tr><tr><td>client</td><td><a href="../../accounts-api/account/"><code>account</code></a></td><td><p>A reference to the client Account object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
    "id": "ACC-1234-4444",
    "href": "/accounts/accounts/ACC-1234-4444",
    "name": "Best LLC",
    "icon": "/static/ACC-1234-4444/account.png"
}
</code></pre></td></tr><tr><td>vendor</td><td><code>account</code></td><td><p>A reference to the vendor Account object. </p><p>Example:</p><pre class="language-json" data-overflow="wrap"><code class="lang-json">{
    "id": "ACC-1234-1234",
    "href": "/accounts/accounts/ACC-1234-1234",
    "name": "Microsoft",
    "icon": "/static/ACC-1234-1234/account.png"
}
</code></pre></td></tr><tr><td>status</td><td><code>enum</code></td><td>The status of the override. Possible values: <code>Active</code> or <code>Disabled</code>. </td></tr><tr><td>externalId</td><td><code>string</code></td><td><p>Reference number. This value is optional.</p><p>Example: bill-12345609</p></td></tr><tr><td>notes</td><td><code>string</code></td><td><p>Notes associated with the override.</p><p>Example: Based on the reporting figures, we decided to move this client to manual billing.</p></td></tr><tr><td>audit</td><td><code>AuditObject</code></td><td><p>Audit object with possible entries: Created or Updated. </p><p>Example:</p><pre class="language-json"><code class="lang-json">{
  "created": { "at": "...", "by": { } },
  "updated": { "at": "...", "by": { } }
}
</code></pre></td></tr></tbody></table>

