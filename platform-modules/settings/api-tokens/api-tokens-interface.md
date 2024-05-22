---
description: Learn about the fields and actions available on the API tokens page.
---

# API Tokens Interface

## API tokens page <a href="#agreements-interface" id="agreements-interface"></a>

The **API tokens** page, located under **Settings** > **API tokens**, displays all tokens in your account.

<figure><img src="../../../.gitbook/assets/image (330).png" alt=""><figcaption><p>API tokens page page</p></figcaption></figure>

For each token, you can view the following information:

* **API token** - Displays the name of the token and its marketplace identifier.
* **Modules** - Displays the total number of modules that the API token has access to. If there is only one module, the module name is displayed.
* **Created** **by** - Displays the name and marketplace ID of the person who created the token.&#x20;
* **Date created** - Displays the date and time when the token was created.
* **Last access** - Displays the date and time when the token was last used.
* **Status** - Displays the current status of the token. Possible statuses include:
  * **Active** - The token has been authenticated in the account and will allow access to the endpoint.
  * **Disabled** - The token has been temporarily deactivated. Any attempts to access the endpoint will return an error.
  * **Deleted** - The token has been permanently removed from the system.&#x20;
* **Actions** - Displays options that allow you to manage the API token. Depending on the status of the token, you can enable or disable a token, delete the token permanently, or edit token details.

## Token details page

The details page of a token displays additional information about the token. You can open the details page by clicking the token name on the API tokens page.

<details>

<summary>What can I do on this page?</summary>

From the details page, you can complete the following tasks:&#x20;

* [Edit an API token](edit-api-token.md)
* [Delete an API token](delete-api-token.md)
* [Enable or disable a token](enable-or-disable-api-token.md)

</details>

<figure><img src="../../../.gitbook/assets/image (331).png" alt=""><figcaption><p>Details page of an API token</p></figcaption></figure>

When you open the details page, it shows the token's name, marketplace ID, and status. The page also contains the following tabs that display corresponding information:

* **General** - Displays the token's description and allows you to show, hide, and copy the values.&#x20;
* **Modules** - Displays the platform modules that the API token has been granted access to within the scope of an account.
* **Details** - Displays the date and time information for your selected token, for example, the date and time when the token was created.

## Related topics

{% content-ref url="./" %}
[.](./)
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

{% content-ref url="enable-or-disable-api-token.md" %}
[enable-or-disable-api-token.md](enable-or-disable-api-token.md)
{% endcontent-ref %}

{% content-ref url="delete-api-token.md" %}
[delete-api-token.md](delete-api-token.md)
{% endcontent-ref %}
