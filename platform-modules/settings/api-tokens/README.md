---
description: Learn about API tokens and how to access the API tokens page.
---

# API tokens

## About API tokens

The Marketplace Platform uses API tokens to authenticate requests to the [REST API](../../../developer-resources/rest-api/) .  Your API token must be included in the "**Authorization**" HTTP header with the "**Bearer**" prefix for authentication. For example, the following request could be used to retrieve a list of Buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas like GitHub or client-side code. All API requests must be made over **HTTPS**. Calls made over plain HTTP will fail. API requests without authentication will also fail.

## How to access the API tokens page

As an account administrator, you can access the **API tokens** page by navigating to the main menu and selecting **Settings** > **API tokens**.&#x20;

From the **API tokens** page, you can:

* Create new tokens and then use those tokens to access different workflows and modules within the Marketplace Platform.
* View a list of your tokens.&#x20;
* Copy the token values for use in your application.
* Delete a token if it's no longer needed.
* Disable a token temporarily and then re-enable it as needed.

## Related topics

{% content-ref url="api-tokens-interface.md" %}
[api-tokens-interface.md](api-tokens-interface.md)
{% endcontent-ref %}

{% content-ref url="create-api-tokens.md" %}
[create-api-tokens.md](create-api-tokens.md)
{% endcontent-ref %}

{% content-ref url="edit-api-tokens.md" %}
[edit-api-tokens.md](edit-api-tokens.md)
{% endcontent-ref %}

{% content-ref url="copy-an-api-token.md" %}
[copy-an-api-token.md](copy-an-api-token.md)
{% endcontent-ref %}

{% content-ref url="enable-or-disable-api-tokens.md" %}
[enable-or-disable-api-tokens.md](enable-or-disable-api-tokens.md)
{% endcontent-ref %}

{% content-ref url="delete-an-api-token.md" %}
[delete-an-api-token.md](delete-an-api-token.md)
{% endcontent-ref %}
