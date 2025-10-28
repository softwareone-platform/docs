# Update Licensee

Updates the licensee object.

You can update the licensee `Seller` object, except the `status` (which is managed through the `disable`, `enable`,  `delete` endpoints), `buyersId` , and `sellersId.`

{% openapi-operation spec="marketplace-accounts-api" path="/public/v1/accounts/licensees/{id}" method="put" %}
[OpenAPI marketplace-accounts-api](https://api.platform.softwareone.com/public/v1/accounts/openapi.json)
{% endopenapi-operation %}
