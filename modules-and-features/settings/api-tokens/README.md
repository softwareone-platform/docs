# API Tokens

The Marketplace Platform uses API tokens to authenticate requests to the [REST API](../../../developer-resources/rest-api/).

Your API token must be included in the **Authorization** HTTP header with the **Bearer** prefix for authentication. For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas like GitHub or client-side code.&#x20;

All API requests must be made over **HTTPS**. Calls made over plain HTTP will fail. API requests without authentication will also fail.

As an account administrator, you can view and manage your tokens on the **API tokens** page. The page is available under **Settings** in the main menu.

<figure><img src="../../../.gitbook/assets/API token.png" alt=""><figcaption><p>API tokens page</p></figcaption></figure>

The page shows all tokens associated with your account. For each token, you can view details such as the token's name, the creator's name, the creation date, and the token's current [status](token-states.md).&#x20;

You also have action links that allow you to enable, disable, or delete the token. Additionally, you can edit the token's details.

## Viewing token details

To view the details page of a token, select the token in the **API token** column.&#x20;

<figure><img src="../../../.gitbook/assets/TokenDetails.png" alt=""><figcaption></figcaption></figure>

When you open the details page, it shows the token's name, marketplace ID, and status. The page also contains the following tabs that display corresponding information:

<table><thead><tr><th width="165">Tab</th><th>Description</th></tr></thead><tbody><tr><td><strong>General</strong></td><td>Displays the token's description and allows you to show, hide, and copy the values.</td></tr><tr><td><strong>Modules</strong></td><td>Displays the modules that the API token has been granted access to within the scope of an account.</td></tr><tr><td><strong>Details</strong></td><td>Displays the date and time information for your selected token, for example, the date and time when the token was created.</td></tr><tr><td><strong>Audit trail</strong></td><td>Displays an audit trail of all changes and events. To learn more, see <a href="https://docs.platform.softwareone.com/modules-and-features/settings/audit-trail">Audit Trail</a>.</td></tr></tbody></table>

## Additional actions

You can perform various actions on the details page. The available actions depend on the token's current status:

* [Edit the existing token](edit-api-token.md)
* [Copy your API token](copy-api-token.md)
* [Delete a token permanently](delete-api-token.md)
* [Enable or disable a token](enable-or-disable-api-token.md)
