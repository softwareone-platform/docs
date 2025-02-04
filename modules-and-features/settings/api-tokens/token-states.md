# Token States

A token can have multiple states during its lifecycle in the Marketplace Platform.

The following diagram shows the possible states and the transition between these states:

<figure><img src="../../../.gitbook/assets/Token.png" alt=""><figcaption><p>API token state transition</p></figcaption></figure>

These states are displayed as Status within the platform. They are also displayed as an icon beside the token name and ID on the details page.

<table><thead><tr><th width="124">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Active</strong></td><td><p>The token has been authenticated in the account. </p><p></p><p>It will allow access to the endpoint.</p></td></tr><tr><td><strong>Disabled</strong></td><td><p>The token has been temporarily deactivated. </p><p></p><p>Any attempts to access the endpoint will return an error.</p></td></tr><tr><td><strong>Deleted</strong></td><td><p>The token has been permanently removed from the system. </p><p></p><p>This state is not visible to the client or vendor account users.</p></td></tr></tbody></table>

## Related topics

{% content-ref url="create-api-token.md" %}
[create-api-token.md](create-api-token.md)
{% endcontent-ref %}

{% content-ref url="edit-api-token.md" %}
[edit-api-token.md](edit-api-token.md)
{% endcontent-ref %}

{% content-ref url="copy-api-token.md" %}
[copy-api-token.md](copy-api-token.md)
{% endcontent-ref %}

{% content-ref url="delete-api-token.md" %}
[delete-api-token.md](delete-api-token.md)
{% endcontent-ref %}

{% content-ref url="enable-or-disable-api-token.md" %}
[enable-or-disable-api-token.md](enable-or-disable-api-token.md)
{% endcontent-ref %}
