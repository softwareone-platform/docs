# State Diagram

The following diagram shows the state (status) transition process of a contact on the platform.

<figure><img src="../../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Contact state diagram</p></figcaption></figure>

### State description

<table><thead><tr><th width="135">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>New</strong></td><td>This is the initial status for a new contact.</td></tr><tr><td><strong>Active</strong></td><td>A contact in this state can receive emails from the platform, depending on their preferences.</td></tr><tr><td><strong>Blocked</strong></td><td>A contact in this state will not receive the email, but the platform will generate a message.</td></tr><tr><td><strong>Deleted</strong></td><td>Deleted contacts cannot be used for notifications.</td></tr></tbody></table>
