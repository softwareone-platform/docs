# Enable Account

Enable the previously disabled [Account](https://docs.client.softwareone.com/extensions/dmE39nDvDSpNnt3t1FdJ#account-object) object.

When enabled, the account status will change to `Active` if the account has `ExternalId` assigned or `Enabled` otherwise.

{% swagger src="../../../../.gitbook/assets/accounts.json" path="/v1/accounts/accounts/{id}/enable" method="post" %}
[accounts.json](../../../../.gitbook/assets/accounts.json)
{% endswagger %}
