# Disable Seller

Disables or deactivates the seller object. When the seller has been disabled, the status changes from  `Active` to `Disabled`. Note that disabled sellers can't be used in transactions.

{% openapi-operation spec="marketplace-accounts-api" path="/public/v1/accounts/sellers/{id}/disable" method="post" %}
[OpenAPI marketplace-accounts-api](https://api.platform.softwareone.com/public/v1/accounts/openapi.json)
{% endopenapi-operation %}
