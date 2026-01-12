# State Diagram

The following diagram shows the state (status) transition process of a user within an account in the Marketplace Platform. It shows the possible statuses a user can have.

<figure><img src="../../../../.gitbook/assets/state_diagram_user.png" alt=""><figcaption><p>The state transition diagram of a user.</p></figcaption></figure>

<table><thead><tr><th width="189">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Invited</strong></td><td>The user has been invited to join the account but has not accepted the invite yet. This status remains in place until the invitation is accepted.</td></tr><tr><td><strong>Invitation expired</strong></td><td>The user's invitation has expired because they didn't accept it within 7 days from the send date.</td></tr><tr><td><strong>Active</strong></td><td>The user has accepted the invitation. They can access the account and perform actions based on their permissions.</td></tr><tr><td><strong>Blocked</strong></td><td>The user's access has been restricted. This could be due to terms and conditions violations, security concerns, or at the administrator's discretion.</td></tr><tr><td><strong>Disabled</strong></td><td>The user has been removed from the account and can no longer perform any actions.</td></tr><tr><td><strong>Deleted</strong></td><td>The user no longer exists in the system.</td></tr></tbody></table>
