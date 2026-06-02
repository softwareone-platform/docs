---
description: Learn about the different states of an API token.
---

# Token states

An API token allows you to authenticate requests to the [REST API](../../../developer-resources/rest-api/).

A token can be in one of these states: **Active**, **Disabled**, or **Deleted**. The following diagram shows the transitions between these states:

<figure><img src="../../../.gitbook/assets/state_diagram_apiToken.png" alt=""><figcaption><p>The state transition diagram of an API token.</p></figcaption></figure>

The following table describes the different states:

<table><thead><tr><th width="124">State</th><th>Definition</th></tr></thead><tbody><tr><td><strong>Active</strong></td><td>The token is authenticated and will allow access to the endpoint.</td></tr><tr><td><strong>Disabled</strong></td><td>The token is temporarily deactivated. Any attempts to access the endpoint will return an error.</td></tr><tr><td><strong>Deleted</strong></td><td>The token is permanently removed from the system.</td></tr></tbody></table>
