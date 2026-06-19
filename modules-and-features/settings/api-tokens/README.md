---
description: Learn about creating and managing API tokens in the SoftwareOne Marketplace.
---

# API tokens

The Marketplace Platform uses API tokens to authenticate requests to the [REST API](/broken/pages/c48wsZ6OnZim0prmKKFx).

Your API token must be included in the `Authorization` HTTP header with the **Bearer** prefix for authentication. For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas, such as GitHub or client-side code.&#x20;

All API requests must be made over HTTPS. Requests sent over HTTP or without authentication will fail.

### API tokens page

The **API tokens** page lets account administrators create, view, edit, delete, enable, and disable API tokens.

To open the page, choose **Settings** > **API tokens** from the main menu.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/API token.png" alt=""><figcaption><p>Use the API tokens page to view and manage tokens.</p></figcaption></figure></div>

On the **API tokens** page, you can view details for each token, including the token name, creation date, status, and more.&#x20;

You can also select a token to view detailed information organized across several tabs. These details include the token endpoint and secret, event history, and other token‑specific information. For details, see [View API tokens](view-api-tokens.md).

### Related topics

{% content-ref url="token-states.md" %}
[token-states.md](token-states.md)
{% endcontent-ref %}

{% content-ref url="create-api-token.md" %}
[create-api-token.md](create-api-token.md)
{% endcontent-ref %}

{% content-ref url="view-api-tokens.md" %}
[view-api-tokens.md](view-api-tokens.md)
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
