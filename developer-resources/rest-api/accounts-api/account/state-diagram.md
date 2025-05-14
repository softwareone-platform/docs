# State Diagram

The following diagram shows the status transition process of an account on the platform.

## Client account

<figure><img src="../../../../.gitbook/assets/state_diagram_clientaccount.png" alt=""><figcaption><p>Client account transition</p></figcaption></figure>

## Vendor account

<figure><img src="../../../../.gitbook/assets/state_diagram_vendoraccount.png" alt=""><figcaption><p>Vendor account transition</p></figcaption></figure>

## State description

<table><thead><tr><th width="124">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Enabled</strong></td><td>The account has been created, but it's not fully set up in the system. While the account can be used for transactions, these transactions will not be completed.</td></tr><tr><td><strong>Active</strong></td><td>The account is fully operational within the Marketplace.</td></tr><tr><td><strong>Disabled</strong></td><td>The account is not available for transactions, and no user can sign in or switch to this account.</td></tr></tbody></table>
