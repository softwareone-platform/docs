# Pool Constraint Policies

This is a more high-level setting that facilitates the flow in a way that allows implementing policies for entire Pools instead of a single resource. Thus, a manager can enforce all resources in the Pool to share constraints so that they are applied to all resources in this Pool, while custom resource-specific constraints can still exist and yet override the general policy.

To apply pool constraint policies:

1. On the **Pools** page, select a pool group or its sub-pool.
2. Select the **Constrains** tab and click the edit icon![pencil](https://hystax.com/documentation/optscale/_static/screens/resource_constraints/pencil.png)to enter values in the **TTL** or **Daily expense limit** fields.
3. Click<img src="../../../.gitbook/assets/check.png" alt="pencil" data-size="line"> to save your changes.

<figure><img src="../../../.gitbook/assets/pool_constraint_policies.png" alt=""><figcaption><p>Pool constraint policies</p></figcaption></figure>

{% hint style="info" %}
A constraint won't be visible if the related resource has already been deleted from FinOps or if a resource has been tracked only by imported billing data.
{% endhint %}
