# API Tokens

The Marketplace Platform uses API tokens to authenticate requests to the [REST API](../../../developer-resources/rest-api/).

Your API token must be included in the **Authorization** HTTP header with the **Bearer** prefix for authentication. For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas like GitHub or client-side code.&#x20;

All API requests must be made over **HTTPS**. Calls made over plain HTTP will fail. API requests without authentication will also fail.

As an account administrator, you can view and manage your tokens on the **API tokens** page.

<figure><img src="../../../.gitbook/assets/API token.png" alt=""><figcaption><p>API tokens page</p></figcaption></figure>

The page displays all tokens that have been created. For each token, you can view the following information:

* **API token** - Displays the name of the token and its marketplace identifier.
* **Modules** - Displays the total number of modules that the token has access to. In cases where only one module is within the scope, the module name is displayed.
* **Created** **by** - Displays the name and marketplace ID of the person who created the token.&#x20;
* **Date created** - Displays the date and time when the token was created.
* **Last access** - Displays the date and time when the token was last used.
* **Status** - Displays the current status of the token. For more information on the status, see [Token States](token-states.md).
* **Actions** - Displays options that allow you to manage the API token. Depending on the status of the token, you can enable or disable a token, delete the token permanently, or edit the token details.

## Viewing token details

To view the details page of a token, select the token in the **API token** column.&#x20;

From the details page, you can complete the following tasks:

* [Edit a token](edit-api-token.md)
* [Delete a token](delete-api-token.md)
* [Enable or disable a token](enable-or-disable-api-token.md)

## Related topics

{% content-ref url="token-states.md" %}
[token-states.md](token-states.md)
{% endcontent-ref %}

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
