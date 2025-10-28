# State Diagram

The following diagram shows the possible states for the terms and conditions object in the Marketplace Platform and the transition between these states:

<figure><img src="../../../../.gitbook/assets/Terms (1).png" alt=""><figcaption><p>The state transition diagram of a terms object.</p></figcaption></figure>

<table><thead><tr><th width="154">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The term object is being created by the vendor. It is not visible to the clients in the marketplace.</td></tr><tr><td><strong>Pending</strong></td><td>The vendor has submitted the terms to SoftwareOne Operations for review and publishing.</td></tr><tr><td><strong>Published</strong></td><td>The terms object has been published and is visible in the Marketplace.</td></tr><tr><td><strong>Unpublished</strong></td><td>The terms object has been unpublished and is no longer visible in the Marketplace.</td></tr><tr><td><strong>Deleted</strong></td><td>The object no longer exists, meaning it's no longer part of the product definition and can't be used.</td></tr></tbody></table>
