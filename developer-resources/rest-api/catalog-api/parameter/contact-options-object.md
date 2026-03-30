# Contact Options Object

The “Contact” type parameter is one of the components that produces object type output value. It also provides some out-of-the-box validation, such as checking for mandatory fields and enforcing proper email and phone number values, contributing to elaborate data collection.

The value type is `object`.

<table><thead><tr><th width="161">Field</th><th width="214">Type</th><th></th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>The label of the widget. </p><p>Example: Buyer contact</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Define buyer contact</p></td></tr><tr><td>defaultValue</td><td><p>One of: </p><p><code>none</code><br><code>buyer</code><br><code>licensee</code><br><code>currentlySignedInUser</code></p></td><td><p>(optional) Default value. </p><p>Example:  Buyer</p></td></tr><tr><td>phoneMandatory</td><td><code>bool</code></td><td>(optional) Phone number field is optional by default, this control allows vendor to make it a mandatory field.</td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Seller contact",
  "hintText": "Provide seller contact",
  "defaultValue": "Seller",
  "phoneMandatory": true
}
```
{% endcode %}

### Value Fields <a href="#value-fields" id="value-fields"></a>

<table><thead><tr><th width="140">Field</th><th width="148">Type</th><th>Description</th></tr></thead><tbody><tr><td>firstName</td><td><code>string</code></td><td><p>First name of the contact. </p><p>Example: John</p></td></tr><tr><td>lastName</td><td><code>string</code></td><td><p>Last name of the contact.</p><p>Example: Doe</p></td></tr><tr><td>email</td><td><code>string</code></td><td><p>Email address of the contact. </p><p>Example: johndoe@example.com</p></td></tr><tr><td>phone</td><td><code>phone</code></td><td><p>Phone number with international code. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{ 
  "prefix": "+34",
  "number": "660707172"
}
</code></pre></td></tr></tbody></table>

### Value Example <a href="#value-example" id="value-example"></a>

{% code lineNumbers="true" %}
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "email": "john.smith@example.com",
  "phone": { 
      "prefix": "+34",
      "number": "660707172"
  }
}
```
{% endcode %}
