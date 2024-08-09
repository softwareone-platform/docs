# User States

The Marketplace Platform supports various states (also known as status) for users in the system.&#x20;

The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/image-20230929-163355 (1).png" alt=""><figcaption><p>User state transition</p></figcaption></figure>

Note that the Marketplace Platform supports various account types, including vendor and client, so not all states might be visible to you.

<table><thead><tr><th width="186">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Invited</strong></td><td><p>The user has been invited to join an account in the Marketplace Platform, but they have not accepted the invitation. </p><p></p><p>This status remains in place until the invitation is accepted.</p></td></tr><tr><td><strong>Invitation Expired</strong></td><td>The user's invitation has expired because they didn't accept the invitation within seven days from when it was sent.</td></tr><tr><td><strong>Active</strong></td><td>The user can access the account and perform the required operations based on their permissions.</td></tr><tr><td><strong>Blocked</strong></td><td><p>The user has been restricted from accessing the account. </p><p></p><p>This could be due to terms and conditions violations, security concerns, or at the administrator's discretion.</p></td></tr><tr><td><strong>Disabled</strong></td><td>The user has been removed from the account. They cannot perform any operation within the account.</td></tr><tr><td><strong>Deleted</strong></td><td>The user no longer exists in the system.</td></tr></tbody></table>
