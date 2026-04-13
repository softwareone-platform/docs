---
description: Learn about creating and managing API tokens in the SoftwareOne Marketplace.
---

# API Tokens

The Marketplace Platform uses API tokens to authenticate requests to the [REST API](../../../developer-resources/rest-api/).

Your API token must be included in the **Authorization** HTTP header with the **Bearer** prefix for authentication. For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas, like GitHub or client-side code.&#x20;

{% hint style="info" %}
All API requests must be made over **HTTPS**. Calls made over plain **HTTP** will fail. API requests without authentication will also fail.
{% endhint %}

### Accessing API tokens

The **API tokens** page allows account administrators to create and view API tokens. Administrators can also edit, delete, enable, or disable a token.

To navigate to the **API tokens** page, select the main menu, then choose **Settings** > **API tokens**. The list of tokens is displayed:

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/API token.png" alt=""><figcaption><p>Use the API tokens page to view and manage tokens.</p></figcaption></figure></div>

On the **tokens** page, you can view various details for each token, including the token name, creation date, status, and more.&#x20;

You can also select a token to view detailed information organized across several tabs. The information available includes the token endpoint and secret, a record of events or logs for the statement, and more. For details, see [View API tokens](view-api-tokens.md).

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
