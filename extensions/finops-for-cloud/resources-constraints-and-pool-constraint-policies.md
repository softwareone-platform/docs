# Resources Constraints and Pool Constraint Policies

To address the ever-dynamic cloud infrastructure where resources are being created and deleted continuously, FinOps for Cloud introduces a set of tools to help limit the related expenses and the lifetime of individual assets.&#x20;

The following feature is implemented in the form of _constraints_ that you can set for a specific resource or generally for a pool. Two constraint types can be set:

* **TTL** - Represents time to live. A resource should not live for more than the specified period.&#x20;
  * For a resource, specify a date and time.&#x20;
  * For a pool, input an integer between 1 and 720 hours.
* **Daily expenses limit** - The resource spending should not exceed the specified amount in dollars. Input as integer, min $ 1, 0 - unlimited.

When FinOps discovers active resources in the connected source, it checks that they don't violate any existing pool constraints that were applied as policies before.

When a resource hits a constraint, both the Manager and Owner of the resource are alerted through email. If a resource is unassigned, alerts are sent to the organization managers. An exclamation mark also appears next to the pool name on the **Pools** page.

{% hint style="info" %}
FinOps for Cloud sends notifications about violated constraints and doesn't interact with the connected source itself to perform any constraint-related adjustments.
{% endhint %}

## Assigning resources constraints <a href="#resources-constraints" id="resources-constraints"></a>

Follow these steps to assign resource constraints:

1. On the **Resources** page, select the required resource. The details page of your selected resource opens.
2. Select the **Constraints** tab.

<figure><img src="../../.gitbook/assets/resources_constraints.png" alt=""><figcaption><p>Constraints tab</p></figcaption></figure>

3. On the **Constraints** tab, use the slider to enable the required setting, and then click edit ![pencil](https://hystax.com/documentation/optscale/_static/screens/resource_constraints/pencil.png) to enter the value. Click<img src="../../.gitbook/assets/check.png" alt="pencil" data-size="line"> to save your changes.

<figure><img src="../../.gitbook/assets/resources_constraints_tab.png" alt=""><figcaption><p>Available constraint type</p></figcaption></figure>

{% hint style="info" %}
If a resource doesn't have a specific constraint set, it inherits the policies from its Pool. However, the resource owner or manager can override an existing Pool constraint policy for an individual resource by issuing a custom constraint for any given asset.
{% endhint %}

## Pool constraint policies <a href="#pool-constraint-policies" id="pool-constraint-policies"></a>

This is a more high-level setting that facilitates the flow in a way that allows implementing policies for entire Pools instead of a single resource. Thus, a manager can enforce all resources in the Pool to share constraints so that they are applied to all resources in this Pool, while custom resource-specific constraints can still exist and yet override the general policy.

To apply pool constraint policies:

1. On the **Pools** page, select a pool group or its sub-pool.
2. Select the **Constrains** tab and click the edit icon![pencil](https://hystax.com/documentation/optscale/_static/screens/resource_constraints/pencil.png)to enter values in the **TTL** or **Daily expense limit** fields.
3. Click<img src="../../.gitbook/assets/check.png" alt="pencil" data-size="line"> to save your changes.

<figure><img src="../../.gitbook/assets/pool_constraint_policies.png" alt=""><figcaption><p>Pool constraint policies</p></figcaption></figure>

{% hint style="info" %}
A constraint won't be visible if the related resource has already been deleted from FinOps or if a resource has been tracked only by imported billing data.
{% endhint %}

## Deleting a pool <a href="#pool-deletion" id="pool-deletion"></a>

You can change the Pool structure by deleting unnecessary pools. The option to delete a pool is unavailable for pools that sub-pools. In such cases, you must delete the sub-pools first. &#x20;

Additionally, to delete a pool, you must have the Manager role in the parent of the pool you want to delete.

{% hint style="warning" %}
Deleting a pool is irreversible. The system will ask for confirmation before deletion.
{% endhint %}

Follow these steps to delete a pool:

1. On the **Pools** page, click the delete icon in the **Actions** column. A delete confirmation message is displayed.
2. Select the **I understand and want to delete this pool** checkbox.&#x20;
3. Click **Delete**.&#x20;

When a pool is deleted, all resources are reassigned to its parent pool, and all rules that used to point to this pool are redirected to its root.
