# Parameter Group

### Parameter Group

Extends the base [ParameterGroup](../../catalog-api/parameter-group/) object within the catalog.

<table><thead><tr><th width="153">Field Name</th><th width="179">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier of the <code>ParameterGroupDefinition</code>. </p><p>Example: PGD-1234-5678-9012</p></td></tr><tr><td><code>revision</code></td><td>unit</td><td><p>Revision number (used for platform-level versioning). </p><p>Example: 3</p></td></tr><tr><td><code>account</code></td><td>object</td><td>The <a href="../../accounts-api/account/"><code>account</code></a> that owns the <code>parameterGroupDefinition</code>.</td></tr><tr><td><code>name</code></td><td>string</td><td><p>A descriptive name for the group. </p><p>Example: Basic info</p></td></tr><tr><td><code>label</code></td><td>string</td><td><p>A translatable value for the step label shown on UI. </p><p>Example: Business details</p></td></tr><tr><td><code>description</code></td><td>string</td><td><p>A description of the group. </p><p>Example: Essential details of a business</p></td></tr><tr><td><code>parameters</code></td><td>object (<a href="./#orderedparametergroup-object"><code>orderedParameter</code></a>)</td><td><p>Parameters included in the group. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "HPAD-233-33-xx3",
    "externalId": "HPAD-233-33-xx3",
    "group": { "id": "HPGR-7373-6782" },
    "scope": "Form",
    "phase": "Request",
    "description": "The description",
    "context": "Case",
    "constraints": {
      "hidden": true,
      "readonly": true,
      "required": false
    },
    "type": "SingleLineText",
    "options": {
      "name": "Favorite color",
      "placeholderText": "Ex: Green",
      "hintText": "Add here your favorite color. It can be any color.",
    },
    "status": "active"
  ]
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> trail of the group. Allowed values: <code>created</code>, <code>updated</code>, or <code>deleted</code>.</td></tr></tbody></table>

### Ordered Parameter Group object <a href="#orderedparametergroup-object" id="orderedparametergroup-object"></a>

This represents a `parameterGroup` already added to a Form. Since the same `parameterGroup` can be added to multiple forms in different order, this entity is needed. If the `parameterGroup` definition changes, this grouped `parameterGroup` also changes.

<table><thead><tr><th width="149">Field Name</th><th width="183">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>parameterGroup</code></td><td>object</td><td><p><a href="./#parameter-group"><code>parameterGroup</code></a></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "PGR-6790-8304-0001",   
  "title": "Parameters",
  "label": "Create agreement",
  "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
}
</code></pre></td></tr><tr><td><code>form</code></td><td><a href="../form/">form</a></td><td><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  id: "FRM-123456"
}
</code></pre></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td>Order of the <code>parameterGroup</code> withing a form. Example: 100</td></tr></tbody></table>

### Ordered Parameter object <a href="#orderedparameter-object" id="orderedparameter-object"></a>

This represents a parameter already added to a group. Since the same parameter can be added to multiple groups in different order, this entity is needed. If the parameter definition changes, this grouped parameter also changes.

<table><thead><tr><th width="179">Field Name</th><th width="212">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>parameter</code></td><td><a href="../parameter-definition/">parameterDefinition</a></td><td><p><a href="../parameter-definition/"><code>parameterDefinition</code></a> of this parameter. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "HPD-1234-1234",
  "name": "Company Name",
  "scope": "Form",
  "type": "TextField"
  ...
}
</code></pre></td></tr><tr><td><code>parameterGroup</code></td><td><a href="./#parameter-group">parameterGroup</a></td><td><p><a href="./#parameter-group">parameterGroup</a></p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "PGR-6790-8304-0001",   
  "title": "Parameters",
  "label": "Create agreement",
  "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
}
</code></pre></td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td><p>Order of the parameter withing a group. </p><p>Example: 100</p></td></tr></tbody></table>

### Parameter Value object <a href="#parametervalue-object" id="parametervalue-object"></a>

Parameter object contains value of the given parameter along with additional information like value and validation error. This is an snapshot of the `groupedParameter` object

Similar to: Order Parameter Object

<table><thead><tr><th width="202">Field Name</th><th width="220">Data Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>A unique identifier for the parameter value object. </p><p>Example: PVH-1234-5678-9012</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>The ID of the parameter in the external system. </p><p>Example: customer_address</p></td></tr><tr><td><code>revision</code></td><td>uint</td><td>Included to support new platform entity revisioning.</td></tr><tr><td><code>parameter</code></td><td>object</td><td><p>The <a href="../parameter-definition/"><code>parameterDefinition</code></a> of this <code>parameterValue</code>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "HPD-1234-1234"
}
</code></pre></td></tr><tr><td><code>name</code></td><td>string</td><td>The name of the parameter.</td></tr><tr><td><code>value</code></td><td>string</td><td>The parametervalue.</td></tr><tr><td><code>displayValue</code></td><td>string</td><td>The display value of the parameter.</td></tr><tr><td><code>displayOrder</code></td><td>integer</td><td>Order of the parameter within the group</td></tr><tr><td><code>scope</code></td><td>string</td><td>The scope of the parameter. Allowed values: <code>form</code> or <code>case</code>.</td></tr><tr><td><code>phase</code></td><td>string</td><td>The parameter phase. Allowed values: <code>request</code> or <code>response</code>.</td></tr><tr><td><code>constraints</code></td><td><a href="../../catalog-api/parameter/constraints-object.md"><code>constraints</code></a></td><td>A snapshot of the parameter definition constrains.</td></tr><tr><td><code>error</code></td><td><p>object</p><p> </p></td><td><p>The standard error object. When specified represents parameter validation error. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "E001234",
  "message": "Incorrect TAX number format"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>The <a href="../../common-api-objects/audit.md"><code>audit</code></a> trail of the parameter.</td></tr></tbody></table>
