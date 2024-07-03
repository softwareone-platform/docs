# Agreement States

In the Marketplace Platform, an agreement can have several states (also known as status). The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/Agreements (2).png" alt=""><figcaption><p>Agreement state transition</p></figcaption></figure>

These states are displayed as **Status** within the platform. They are also displayed as an icon beside the agreement name and ID on the details page.&#x20;

<table><thead><tr><th width="210">Agreement state</th><th>Description</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The agreement is saved as a draft because the purchase order is saved for later during the ordering process. </td></tr><tr><td><strong>Deleted</strong> </td><td>The draft agreement has been deleted because the draft purchase order associated with the agreement was deleted.</td></tr><tr><td><strong>Provisioning</strong></td><td>The agreement has been sent to the vendor and it's waiting to be fulfilled.</td></tr><tr><td><strong>Failed</strong></td><td>The agreement has failed because the purchase order was canceled by the vendor or SoftwareOne. </td></tr><tr><td><strong>Active</strong> </td><td>The vendor has completed the purchase order and the agreement is now active, meaning it has at least one active subscription and no open orders.</td></tr><tr><td><strong>Updating</strong></td><td>A business transaction or a change order is in progress for at least one subscription item in the agreement.</td></tr><tr><td><strong>Terminated</strong></td><td>The agreement has been terminated, meaning it no longer has any active subscription. </td></tr></tbody></table>
