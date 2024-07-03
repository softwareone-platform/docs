# Token States

An API token can have several states (also known as status) in the Marketplace Platform. The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/Token.png" alt=""><figcaption><p>API token state transition</p></figcaption></figure>

These states are displayed as **Status** within the platform. They are also displayed as an icon beside the token name and ID on the details page.&#x20;

<table><thead><tr><th width="161">Token state</th><th>Description</th></tr></thead><tbody><tr><td><strong>Active</strong></td><td>The token has been authenticated in the account and will allow access to the endpoint.</td></tr><tr><td><strong>Disabled</strong></td><td>The token has been temporarily deactivated. Any attempts to access the endpoint will return an error.</td></tr><tr><td><strong>Deleted</strong></td><td>The token has been permanently removed from the system. This state is not visible to the client or vendor account users.</td></tr></tbody></table>
