# State Diagram

The following diagram shows the possible states for the media object in the Marketplace Platform and the transition between these states:

<figure><img src="../../../../.gitbook/assets/Media (3).png" alt=""><figcaption><p>The state transition diagram of a media object.</p></figcaption></figure>

<table><thead><tr><th width="149">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Draft</strong></td><td>The media is being created. A media object in this state is not visible to clients in the Marketplace.</td></tr><tr><td><strong>Pending</strong></td><td>The media has been submitted to SoftwareOne Operations for review and publishing.</td></tr><tr><td><strong>Published</strong></td><td>The media is now visible in the Marketplace.</td></tr><tr><td><strong>Unpublished</strong></td><td>The media has been unpublished and is not visible in the Marketplace.</td></tr><tr><td><strong>Deleted</strong></td><td>The media no longer exists, meaning it's no longer part of the product definition and can't be used.</td></tr></tbody></table>
