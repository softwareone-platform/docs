# Date Range Options Object

The “Date” parameter provides a calendar-like component to where it is being used. Highly configurable it provides a wide range of functionalities:

1. Calendar control.
2. Date range selection (start-to-end date selection).
3. Date selection control attributes (value can be selected only within a given range of dates).

The value type is `object`.

<table><thead><tr><th width="210">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td><code>string</code></td><td><p>The label of the widget. </p><p>Example: Activation date</p></td></tr><tr><td>hintText</td><td><code>string</code></td><td><p>Provides help text describing what value is expected in control. </p><p>Example: Specify when you want your subscription to be active</p></td></tr><tr><td>dateRange</td><td><code>bool</code></td><td><p>Turning this option on allows selection of two dates (start date &#x26; end date). </p><p>Example: True</p></td></tr><tr><td>minAvailableDate</td><td><code>date</code></td><td><p>(optional) Prevents selection of the date value in the past beyond the value set in this constraint. </p><p>Example: 2024-02-01</p></td></tr><tr><td>maxAvailableDate</td><td><code>date</code></td><td><p>(optional) Prevents selection of the date value in the future beyond the value set in this constraint. </p><p>Example: 2024-12-10</p></td></tr><tr><td>defaultValue</td><td><p>One of <code>singleDate</code> or </p><p><code>dateRange</code></p></td><td><p>(optional) Depending of the dateRange value - default value can be a date range or single date. </p><p>Example: </p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">{
  "date": "2023-10-05"
}
</code></pre></td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "name": "Date of birth",
  "hintText": "Specify your date of birth",
  "dateRange": false,
  "minAvailableDate": "1900-01-01",
  "maxAvailableDate": "2000-12-30",
  "defaultValue":  null
}
```
{% endcode %}

### Value Fields <a href="#value-fields" id="value-fields"></a>

<table><thead><tr><th width="125">Field</th><th width="212">Type</th><th width="415"></th></tr></thead><tbody><tr><td>start</td><td>ISO 8601</td><td><p>Start of date range. </p><p>Example: 2020-12-09</p></td></tr><tr><td>end</td><td>ISO 8601</td><td><p>End of date range. </p><p>Example: 2025-12-09</p></td></tr></tbody></table>

### Example <a href="#example" id="example"></a>

{% code lineNumbers="true" %}
```json
{
  "start": "2020-12-09",
  "end": "2024-12-09"
}
```
{% endcode %}
