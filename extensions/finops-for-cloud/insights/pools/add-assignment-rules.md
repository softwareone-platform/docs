# Configure Assignment Rules

In FinOps for Cloud, you can add new assignment rules from the **Configure assignment rules** option on the **Pools** or **Resource** page.&#x20;

## Configuring new assignment rules

To configure new assignment rules:

1. Do one of the following:
   * On the **Pools** page, select **Configure assignment rules** and then select **Add**.
   * On the **Resources** page, select a resource. Then, on the resource details page, select **Add assignment rule**
2. In the **Name** field, enter a name for the new resource assignment rule.
3. In **Conditions**, select the conditions that must be fulfilled for the rule to become applicable. The following conditions are available:

<table><thead><tr><th width="204">Type</th><th width="185">Key/Value</th><th>Description</th></tr></thead><tbody><tr><td>Name/ID starts with</td><td>string value</td><td>Matches resources where the name or ID begins with the specified value.</td></tr><tr><td>Name/ID ends with</td><td>string value</td><td>Matches resources where the name or ID ends with the specified value.</td></tr><tr><td>Name/ID is</td><td>string value</td><td>Matches resources with an exact name or ID match.</td></tr><tr><td>Name/ID contains</td><td>string value</td><td>Matches resources where the name or ID contains the specified substring.</td></tr><tr><td>Tag is</td><td>key-value pair</td><td>Matches resources with a tag that matches both the specified key and value.</td></tr><tr><td>Tag exists</td><td>key-value pair</td><td>Matches resources that have a tag with the specified key.</td></tr><tr><td>Tag value starts with</td><td>key-value pair</td><td>Matches resources with a tag value starting with the specified value for the given key.</td></tr><tr><td>Source is</td><td>selected row</td><td>Matches resources from a selected data source. Options are presented in a dropdown for selecting the source.</td></tr><tr><td>Resource type is</td><td>string value</td><td>Matches resources where the resource type contains the specified value.</td></tr><tr><td>Region is</td><td>string value</td><td>Matches resources where the region contains the specified value.</td></tr></tbody></table>

5. Add more conditions as relevant.&#x20;
6. In **Assign to**, the matching resource is included in the selected target pool and assigned to an owner.  You can change the values as relevant.&#x20;
7. Select **Create**.&#x20;

When a new rule is added, it is always prioritized across the organization. This means that any discovered resources will first be checked against the conditions of this new rule. If a resource does not meet the new rule's conditions, then it will be checked against the remaining rules in descending order until a matching rule is found.
