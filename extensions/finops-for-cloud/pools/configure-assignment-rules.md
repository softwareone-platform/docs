# Configure Assignment Rules

In FinOps for Cloud, you can add a new assignment rule either from the **Assignment Rules** page or the **Resource** page. Both of these pages are accessible through the left navigation.

## Configuring assignment rules

{% tabs %}
{% tab title="Assignment Rules page" %}
1. On the **Pools** page, click **Configure assignment rules**.
2. On the **Assignment Rules** page, click **Add**.
3. Enter a name for the new automatic resource assignment rule.
4. Select the conditions that must be fulfilled for the rule to become applicable. The following conditions are available:

<table><thead><tr><th width="204">Type</th><th width="185">Key/Value</th><th>Description</th></tr></thead><tbody><tr><td>Name/ID starts with</td><td>string value</td><td>Matches resources where the name or ID begins with the specified value.</td></tr><tr><td>Name/ID ends with</td><td>string value</td><td>Matches resources where the name or ID ends with the specified value.</td></tr><tr><td>Name/ID is</td><td>string value</td><td>Matches resources with an exact name or ID match.</td></tr><tr><td>Name/ID contains</td><td>string value</td><td>Matches resources where the name or ID contains the specified substring.</td></tr><tr><td>Tag is</td><td>key-value pair</td><td>Matches resources with a tag that matches both the specified key and value.</td></tr><tr><td>Tag exists</td><td>key-value pair</td><td>Matches resources that have a tag with the specified key.</td></tr><tr><td>Tag value starts with</td><td>key-value pair</td><td>Matches resources with a tag value starting with the specified value for the given key.</td></tr><tr><td>Source is</td><td>selected row</td><td>Matches resources from a selected data source. Options are presented in a dropdown for selecting the source.</td></tr><tr><td>Resource type is</td><td>string value</td><td>Matches resources where the resource type contains the specified value.</td></tr><tr><td>Region is</td><td>string value</td><td>Matches resources where the region contains the specified value.</td></tr></tbody></table>

5. Add and remove conditions as needed. The matching resource is included in the selected target pool and assigned to an owner.
6. Click **Create**.
{% endtab %}

{% tab title="Resources page" %}
From the Resources page, you can add an assignment rule by clicking **Add Assignment Rule** on a specific resource's details page. This method simplifies the creation of assignment rules for a particular resource by pre-filling relevant fields with the resource's existing data.

1. On the **Resources** page, select a resource.&#x20;
2. On the details page of your selected resource, click **Add assignment rule**.
3. Enter a name and then add conditions as necessary.&#x20;
4. Select the target pool and the owner.
5. Click **Create**.
{% endtab %}
{% endtabs %}

After you've added the rule, the newly created rule is always prioritized across the organization and is put at the top of the list for the discovered resources to be checked against its conditions first. If these are not satisfied, a resource will be checked against the remaining rules in descending order until one is found applicable.
