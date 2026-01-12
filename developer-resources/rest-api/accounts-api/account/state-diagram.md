# State Diagram

The Marketplace Platform provides three distinct user interfaces, namely the Client Portal, Vendor Portal, and Operations Portal. This topic describes how the account object transitions through different lifecycle states in the Marketplace Platform.

{% hint style="info" %}
The diagrams show different transitions depending on whether the account is a Client/Partner or a Vendor, but the underlying statuses are the same.
{% endhint %}

### Client account

The following diagram shows how a client/partner account moves between states through operations like enable, activate, and disable.

<figure><img src="../../../../.gitbook/assets/state_diagram_clientaccount.png" alt=""><figcaption><p>The state transition diagram of a client account.</p></figcaption></figure>

### Vendor account

The following diagram shows how a vendor account progresses between states.

<figure><img src="../../../../.gitbook/assets/state_diagram_vendoraccount.png" alt=""><figcaption><p>The state transition diagram of a vendor account.</p></figcaption></figure>

<table><thead><tr><th width="124">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>New</strong></td><td>This is the default state of a newly created account. This state is not visible on the interface.</td></tr><tr><td><strong>Enabled</strong></td><td>The account has been created, but it has not been fully set up yet in the system. While the account can be used for transactions, these transactions will not be completed.</td></tr><tr><td><strong>Active</strong></td><td>The account is fully operational in the Marketplace.</td></tr><tr><td><strong>Disabled</strong></td><td>The account is not available for transactions, and users cannot sign in or switch to this account.</td></tr></tbody></table>
