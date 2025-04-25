# Delete Pools

You can change the Pool structure by deleting unnecessary pools. The option to delete a pool is unavailable for pools that include sub-pools. In such cases, you must delete the sub-pools first. &#x20;

Additionally, to delete a pool, you must have the Manager role in the parent of the pool you want to delete.

{% hint style="warning" %}
Deleting a pool is irreversible. The system will ask for confirmation before deletion.
{% endhint %}

## Deleting a pool <a href="#pool-deletion" id="pool-deletion"></a>

To delete a pool:

1. On the **Pools** page, select the delete icon in the **Actions** column. A delete confirmation message is displayed.
2. Select the **I understand and want to delete this pool** checkbox.&#x20;
3. Select **Delete**.&#x20;

When a pool is deleted, all resources are reassigned to its parent pool. Additionally, all rules that used to point to this pool are redirected to its root.
