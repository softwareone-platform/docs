# Update Licensee

Update the licensee object.

You can update the licensee `Seller` Object, except the `status` (which is managed through the `disable`, `enable`, `delete`endpoints) `buyers id` and `sellers id.`

{% swagger src="../../../../.gitbook/assets/accounts.json" path="/v1/accounts/licensees/{id}" method="put" %}
[accounts.json](../../../../.gitbook/assets/accounts.json)
{% endswagger %}
