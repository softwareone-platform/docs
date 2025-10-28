# Enable Buyer

Enables a buyer that was previously disabled. When enabled, the buyer's status changes to `Active`  if the buyer has `ExternalId` assigned or enabled.

{% openapi-operation spec="marketplace-accounts-api" path="/public/v1/accounts/buyers/{id}/enable" method="post" %}
[OpenAPI marketplace-accounts-api](https://api.platform.softwareone.com/public/v1/accounts/openapi.json)
{% endopenapi-operation %}
