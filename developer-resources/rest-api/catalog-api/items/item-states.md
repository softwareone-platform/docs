# State Diagram

The following diagram shows the possible states an item may have in the Marketplace Platform and the transition between these states:

<figure><img src="../../../../.gitbook/assets/Item (3).png" alt=""><figcaption><p>The state transition diagram of an item.</p></figcaption></figure>

<table><thead><tr><th width="144">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The item object is being created by the vendor. This object is not visible to client accounts.</td></tr><tr><td><strong>Review</strong></td><td>The vendor has submitted the item to SoftwareOne Operations for review and publishing. SoftwareOne Operations will add the ERP item ID before publishing.</td></tr><tr><td><strong>Published</strong></td><td>The item object is available in the marketplace.</td></tr><tr><td><strong>Unpublished</strong></td><td>The item object is not available in the marketplace.</td></tr><tr><td><strong>Deleted</strong></td><td>The item object no longer exists, meaning it's no longer part of the product definition and can't be used anymore.</td></tr></tbody></table>

