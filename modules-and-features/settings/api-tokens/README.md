# API Tokens

The Marketplace Platform uses API tokens to authenticate requests to the [REST API](../../../developer-resources/rest-api/).

Your API token must be included in the **Authorization** HTTP header with the **Bearer** prefix for authentication. For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas like GitHub or client-side code.&#x20;

All API requests must be made over **HTTPS**. Calls made over plain HTTP will fail. API requests without authentication will also fail.

## API tokens interface <a href="#agreements-interface" id="agreements-interface"></a>

Account administrators can access the **API tokens** page by selecting **Settings** > **API tokens** from the main menu.

<figure><img src="../../../.gitbook/assets/API token.png" alt=""><figcaption><p>API tokens page</p></figcaption></figure>

The page displays all tokens that have been created in your account. For each token, you can view the following information:

* **API token** - Displays the name of the token and its marketplace identifier.
* **Modules** - Displays the total number of modules that the token has access to. In cases where only one module is within the scope, the module name is displayed.
* **Created** **by** - Displays the name and marketplace ID of the person who created the token.&#x20;
* **Date created** - Displays the date and time when the token was created.
* **Last access** - Displays the date and time when the token was last used.
* **Status** - Displays the current status of the token. For more information on the status, see [Token States](token-states.md).
* **Actions** - Displays options that allow you to manage the API token. Depending on the status of the token, you can enable or disable a token, delete the token permanently, or edit token details.

## Token details page

The details page of a token displays additional information about the token. You can open the details page by clicking the token name on the API tokens page.

<details>

<summary>What can I do on this page?</summary>

From the details page, you can complete the following tasks:&#x20;

* [Edit a token](edit-api-token.md)
* [Delete a token](delete-api-token.md)
* [Enable or disable a token](enable-or-disable-api-token.md)

</details>

<figure><img src="../../../.gitbook/assets/TokenDetails.png" alt=""><figcaption><p>Details page of a token</p></figcaption></figure>

When you open the details page, it shows the token's name, marketplace ID, and status. The page also contains the following tabs that display corresponding information:

* **General** - Displays the token's description and allows you to show, hide, and copy the values.&#x20;
* **Modules** - Displays the modules that the API token has been granted access to within the scope of an account.
* **Details** - Displays the date and time information for your selected token, for example, the date and time when the token was created.
* **Audit trail** - Displays an audit trail of all changes and events within the token account. For each audit record, you can view the log details and summary. To learn more, see [Audit Trail](https://docs.platform.softwareone.com/modules-and-features/settings/audit-trail).

## Related topics

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/token-states" %}
[Token States](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/token-states)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/create-api-token" %}
[Create API Token](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/create-api-token)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/edit-api-token" %}
[Edit API Token](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/edit-api-token)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/copy-api-token" %}
[Copy API Token](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/copy-api-token)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/delete-api-token" %}
[Delete API Token](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/delete-api-token)
{% endcontent-ref %}

{% content-ref url="https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/enable-or-disable-api-token" %}
[Enable or Disable API Token](https://app.gitbook.com/s/rouC21YfVpuUxysQFTrr/modules-and-features/settings/api-tokens/enable-or-disable-api-token)
{% endcontent-ref %}
