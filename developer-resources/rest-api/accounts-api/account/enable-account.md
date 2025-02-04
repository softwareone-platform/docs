# Enable Account

Enable the previously disabled [Account](https://docs.client.softwareone.com/extensions/dmE39nDvDSpNnt3t1FdJ#account-object) object.

When enabled, the account status will change to `Active` if the account has `ExternalId` assigned or `Enabled` otherwise.

{% swagger src="../../../../.gitbook/assets/swaggerQA_31_01_2025.json" path="/v1/accounts/accounts/{id}/enable" method="post" %}
[swaggerQA_31_01_2025.json](../../../../.gitbook/assets/swaggerQA_31_01_2025.json)
{% endswagger %}
