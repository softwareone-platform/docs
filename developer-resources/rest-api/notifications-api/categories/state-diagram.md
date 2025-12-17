# State Diagram

The following diagram shows the state (status) transition process of a notification category in the platform.

<figure><img src="../../../../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption><p>The state transition diagram of a category.</p></figcaption></figure>

### State description

<table><thead><tr><th width="135">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>New</strong></td><td>This is the initial status for a newly created category. This state is not visible on the interface.</td></tr><tr><td><strong>Published</strong></td><td>The category has been published and is visible on the platform. When a category is created, it is automatically set to the published state. By default, it is enabled for everyone. Users can disable the category in their notification settings if they choose to do so.</td></tr><tr><td><strong>Unpublished</strong></td><td>The category has been published and is visible on the platform. However, a Notification Category in this state cannot be used and is therefore not visible on the platform. An unpublished category can be revived and changed back to a published state.</td></tr><tr><td><strong>Deleted</strong></td><td>The category has been deleted. When a category is deleted, all configurations for that category across all accounts are also removed.</td></tr></tbody></table>
