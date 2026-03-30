# Email Options Object

The “Email” parameter type provides a form element that does email validation out-of-the-box following RFC 5322 guides.

<table><thead><tr><th width="185">Field</th><th width="215">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>The label of the widget. </p><p>Example: Email</p></td></tr><tr><td>placeholderText</td><td><code>string</code></td><td><p>Provides default text within the control when no selection is not made. </p><p>Example: email@org.com</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Enter email address</p></td></tr><tr><td>defaultValue</td><td><code>none</code> or <code>currentlySignedInUser</code></td><td>(optional) Default value.</td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Email",
  "placeholderText": "email@org.com",
  "hintText": "Enter email address",
}
```
{% endcode %}
