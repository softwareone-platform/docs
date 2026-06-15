# Parameter Group

The Parameter Group object extends the base [ParameterGroup](../../catalog-api/parameter-group/) object within the catalog.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="146">Field</th><th width="168">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td><p>Unique identifier of the <code>parameterGroupDefinition</code>. </p><p>Example: PGD-1234-5678-9012</p></td></tr><tr><td><code>revision</code></td><td>unit, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td><p>(Read-only) The revision number used for platform-level versioning.</p><p>Example: 3</p></td></tr><tr><td><code>account</code></td><td>object, core</td><td>The <a href="../../accounts-api/account/"><code>account</code></a> that owns the <code>parameterGroupDefinition</code>.</td></tr><tr><td><code>name</code></td><td>string, core</td><td><p>A descriptive name for the group. </p><p>Example: Basic info</p></td></tr><tr><td><code>label</code></td><td>string, core</td><td><p>A translatable value for the step label shown on UI. </p><p>Example: Business details</p></td></tr><tr><td><code>description</code></td><td>string, core</td><td><p>A description of the group. </p><p>Example: Essential details of a business</p></td></tr><tr><td><code>parameters</code></td><td>object, core</td><td><p>Represents the <a href="./#orderedparametergroup-object"><code>orderedParameter</code></a> object, which contains parameters included in the group. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
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
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Ordered Parameter Group object <a href="#orderedparametergroup-object" id="orderedparametergroup-object"></a>

Represents a `parameterGroup` instance that has already been added to a form. Because the same `parameterGroup` can be reused across multiple forms in a different order, this entity is required. If the `parameterGroup` definition changes, the `parameterGroup` also changes to reflect those updates.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="158">Field</th><th width="151">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>parameterGroup</code></td><td>object</td><td><p>A reference to the <a href="./#parameter-group"><code>parameterGroup</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "PGR-6790-8304-0001",   
  "title": "Parameters",
  "label": "Create agreement",
  "description": "When creating a new agreement with SoftwareOne, you have the option to establish a new Microsoft account or connect it to an existing account you already hold with Microsoft.",
}
</code></pre></td></tr><tr><td><code>form</code></td><td>object, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td><p>Represents the <a href="../form/"><code>form</code></a> object. Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  id: "FRM-123456"
}
</code></pre></td></tr><tr><td><code>displayOrder</code></td><td>integer, core</td><td>The order of the <code>parameterGroup</code> within the form. Example: 100</td></tr></tbody></table>

## Ordered Parameter object <a href="#orderedparameter-object" id="orderedparameter-object"></a>

Represents a parameter that has already been added to a group. Since the same parameter can be added to multiple groups in a different order, this entity is required. If the parameter definition changes, this grouped parameter also changes to reflect those updates.

<table><thead><tr><th width="154">Field</th><th width="140">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>parameter</code></td><td>object</td><td><p>The <a href="../parameter-definition/"><code>parameterDefinition</code></a> of this parameter. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "HPD-1234-1234",
  "name": "Company Name",
  "scope": "Form",
  "type": "TextField"
  ...
}
</code></pre></td></tr><tr><td><code>parameterGroup</code></td><td>object</td><td><p>Represents the <a href="./#parameter-group"><code>parameterGroup</code></a>.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "PGR-6790-8304-0001",   
  "title": "Parameters",
  "label": "Create agreement",
  "description": "When creating a new agreement with SoftwareOne, you can establish a new Microsoft account or connect an existing one.",
}
</code></pre></td></tr><tr><td><code>displayOrder</code></td><td>integer, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td><p>The order of the parameter within the group. </p><p>Example: 100</p></td></tr></tbody></table>

## Parameter Value object <a href="#parametervalue-object" id="parametervalue-object"></a>

The parameter object contains the value of the given parameter, along with additional information such as the value and validation error. This is a snapshot of the `groupedParameter` object.

<table><thead><tr><th width="166">Field</th><th width="145">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td><p>A unique identifier for the parameter value object. </p><p>Example: PVH-1234-5678-9012</p></td></tr><tr><td><code>externalId</code></td><td>string</td><td><p>(Read-only) The ID of the parameter in the external system. </p><p>Example: customer_address</p></td></tr><tr><td><code>revision</code></td><td>uint, core</td><td>(Read-only) Included to support new platform entity revisioning.</td></tr><tr><td><code>parameter</code></td><td>object, core</td><td><p>The <a href="../parameter-definition/"><code>parameterDefinition</code></a> of this <code>parameterValue</code>. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "HPD-1234-1234"
}
</code></pre></td></tr><tr><td><code>name</code></td><td>string, core</td><td>The name of the parameter.</td></tr><tr><td><code>value</code></td><td>string, core</td><td>(Optional) The parameter value.</td></tr><tr><td><code>displayValue</code></td><td>string</td><td>(Optional) The display value of the parameter.</td></tr><tr><td><code>displayOrder</code></td><td>integer, core</td><td>The order of the parameter within the group</td></tr><tr><td><code>scope</code></td><td>string, core</td><td>The scope of the parameter. Allowed values are <code>form</code> or <code>case</code>.</td></tr><tr><td><code>phase</code></td><td>string, core</td><td>The parameter phase. Allowed values:<code>request</code> or <code>response</code>.</td></tr><tr><td><code>constraints</code></td><td>object</td><td>Represents the <a href="../../catalog-api/parameter/constraints-object.md"><code>constraints</code></a> <code>parameter</code>, which stores a snapshot of the parameter's definition.</td></tr><tr><td><code>error</code></td><td><p>object</p><p> </p></td><td><p>(Optional) Represents the error object. When specified represents a parameter validation error. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "id": "E001234",
  "message": "Incorrect TAX number format"
}
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
