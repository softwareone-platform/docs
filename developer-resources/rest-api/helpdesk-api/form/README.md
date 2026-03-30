# Form

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="161">Field Name</th><th width="170">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the form. </p><p>Example: FRM-1234-4567</p></td></tr><tr><td><code>revision</code></td><td>unit</td><td>Revision number (used for platform-level versioning).</td></tr><tr><td><code>name</code></td><td>string</td><td><p>A descriptive name for the form. </p><p>Example: User report</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the form. </p><p>Example: Form to support billing issues</p></td></tr><tr><td><code>status</code></td><td>string</td><td>The current state of the form. Allowed values:<code>published</code> or <code>unpublished</code>.</td></tr><tr><td><code>parameterGroups</code></td><td>object</td><td><p><a href="../parameter-group/#orderedparametergroup-object"><code>orderedParameterGroup</code></a> containing parameters of the form. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
   {
     parameterGroup: {
      "id": "PGR-6790-8304-0001",   
      "title": "Parameters",
      "label": "Create agreement",
      "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
    },
    displayOrder: 100
  }
]
</code></pre></td></tr><tr><td><code>account</code></td><td>object</td><td>The <a href="../../accounts-api/account/"><code>account</code></a> that owns the form. </td></tr><tr><td><code>audit</code></td><td>object</td><td>A reference to the <a href="../../common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>
