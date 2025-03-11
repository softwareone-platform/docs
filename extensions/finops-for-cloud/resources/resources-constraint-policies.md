# Resources Constraint Policies

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

<figure><img src="../../../.gitbook/assets/resources_constraints.png" alt=""><figcaption><p>Constraints tab</p></figcaption></figure>

3. Use the slider to enable the required setting, and then click edit ![pencil](https://hystax.com/documentation/optscale/_static/screens/resource_constraints/pencil.png) to enter the value. Click<img src="../../../.gitbook/assets/check.png" alt="pencil" data-size="line"> to save your changes.

<figure><img src="../../../.gitbook/assets/resources_constraints_tab.png" alt=""><figcaption><p>Available constraint type</p></figcaption></figure>

{% hint style="info" %}
If a resource doesn't have a specific constraint set, it inherits the policies from its Pool. However, the resource owner or manager can override an existing Pool constraint policy for an individual resource by issuing a custom constraint for any given asset.
{% endhint %}
