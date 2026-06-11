# User

The User object represents a single user on the Marketplace platform.&#x20;

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table data-full-width="false"><thead><tr><th width="175">Field</th><th width="158">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) Primary identifier for the user.</td></tr><tr><td><code>email</code></td><td>string</td><td>The email address of the user.</td></tr><tr><td><code>status</code></td><td>string</td><td><p>(Read-only) The user's status. Allowed values: </p><ul><li><code>New</code></li><li><code>Invited</code></li><li><code>Invitation expired</code></li><li><code>Active</code></li><li><code>Blocked</code></li><li><code>Disabled</code></li><li><code>Deleted</code>. </li></ul><p>The <code>Invited</code> or <code>InvitationExpired</code> statuses apply only if the user has not yet joined the account.</p></td></tr><tr><td><code>name</code></td><td>string, core</td><td>The user's full name.</td></tr><tr><td><code>firstName</code></td><td>string</td><td>The user's first name.</td></tr><tr><td><code>lastName</code></td><td>string</td><td>The user's last name.</td></tr><tr><td><code>phone</code></td><td>object</td><td>The country code and phone number.</td></tr><tr><td><code>accounts</code></td><td>object</td><td>List of accounts that the user is added to; not returned in the user’s account sub‑collection.</td></tr><tr><td><code>currentAccount</code></td><td>object</td><td>The account currently selected by the user.</td></tr><tr><td><code>groups</code></td><td>object</td><td><p>(Read-only) Represents the <a href="../user-groups/#group-object"><code>group</code></a> object containing all groups that the user belongs to.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers><code class="lang-json">[
  {
    "id": "UGR-5116-6265",
    "name": "Administrators"
  },
  {
    "id": "UGR-5116-6565",
    "name": "Fulfillment Managers"
  }
]
</code></pre></td></tr><tr><td><code>buyers</code></td><td>object</td><td>(Read-only) List of all buyers the user can access through their groups. Not defined when the ‘All’ option is selected.</td></tr><tr><td><code>modules</code></td><td>object</td><td>(Read-only) List of all modules the user can access through their groups.</td></tr><tr><td><code>settings</code></td><td>object</td><td>(Optional) Indicates the user’s preferences, including language and regional settings (legacy).</td></tr><tr><td><code>invitation</code></td><td>object</td><td>(Optional) Represents the <code>invitation</code> object. This is included only in the context of an account (within the account sub‑collection) and only when the user has been invited.</td></tr><tr><td><code>invitation.code</code></td><td>string</td><td>(Read-only) (Optional) The invitation code sent to user when they are invited to the platform.</td></tr><tr><td><code>invitation.status</code></td><td>string</td><td>(Read-only) (Optional) Indicates the user's account invitation status.</td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object.</td></tr></tbody></table>

## Examples

{% tabs %}
{% tab title="ACCOUNT CONTEXT" %}
{% code title="USER OBJECT" lineNumbers="true" %}
```json
{
    "id": "USR-3773-5838",    
    "email": "test@testignite.de",
    "status": "Active",
    "firstName": "d",
    "lastName": "d",
    "settings": {
        "cultureCode": "en-US",
        "languageCode": "en-US"
    },
    "name": "d d",
    "account": {
        "id": "ACC-0774-6909",    
        "type": "Client",
        "status": "Active",
        "name": "Ignite Test CDG"
    },    
    "groups": [
        {
            "id": "UGR-5240-4954",          
            "name": "Only Marketplace and Buyer BUY-1089-7077",
            "description": "",
            "account": {
                "id": "ACC-0774-6909",               
                "type": "Client",
                "status": "Active",
                "name": "Ignite Test CDG"
            },
            "logo": "",
            "isDefault": false
        }
    ],
    "buyers": [
        {
            "id": "BUY-1089-7077",           
            "status": "Enabled",
            "address": {
                "addressLine1": "adress1",
                "addressLine2": "adress2",
                "postCode": "88131",
                "city": "city",
                "state": "bavaria",
                "country": "DE"
            },
            "account": {
                "id": "ACC-0774-6909",               
                "type": "Client",
                "status": "Active",
                "name": "Ignite Test CDG"
            },
            "name": "testBuyer"
        }
    ],
    "modules": [
        {
            "id": "MOD-0478",          
            "description": "Buy and manage subscription based licenses.",
            "isConfigurable": true,
            "isEnabledByDefault": true,
            "paid": false,
            "name": "Marketplace",
            "filters": {
                "group.buyers": [
                    "selected",
                    "all"
                ]
            },
            "settings": {
                "sharedAccount": true,
                "configurable": true,
                "default": true,
                "paid": false
            }
        }
    ],
    "invitation": {
        "url": "https://portal.s1.show/accept-invite?code=eyJjb2RlIjoiUzM0dVpsVWNjL0JSRTdpVXFSdFBpN2J4Z3BaY3VXNTFoM2d4WlN6T0xwdz0iLCJhY2NvdW50VXNlcklkIjoiQVVTUi0xMDQwLTg2MzYtNzI2NyJ9",
        "status": "Active"
    },
    "audit": {
        "login": {
            "at": "2024-05-09T14:40:28.886Z"
        },    
        "access": {
            "at": "2024-09-20T14:01:45.603Z"
        },
        "joined": {
            "at": "2024-05-09T14:40:28.886Z"
        },
        "created": {
            "at": "2024-05-09T14:40:28.958Z",
            "by": {
                "id": "TKN-7670-9957",
                "href": "/accounts/api-tokens/TKN-7670-9957",
                "name": "[DO NOT REMOVE] PyraProxy"
            }
        },
        "updated": {
            "at": "2024-09-16T12:33:03.761Z",
            "by": {
                "href": "//"
            }
        }
    }
}

```
{% endcode %}
{% endtab %}

{% tab title="GLOBAL CONTEXT" %}
{% code title="USER OBJECT" lineNumbers="true" %}
```json
{
    "id": "USR-3773-5838",    
    "email": "test@testignite.de",
    "status": "Active",
    "firstName": "d",
    "lastName": "d",
    "settings": {
        "cultureCode": "en-US",
        "languageCode": "en-US"
    },
    "name": "d d",
    "accounts": [
      {
          "id": "ACC-0774-6909",         
          "type": "Client",
          "status": "Active",
          "name": "Ignite Test CDG"
      }
    ],
    "currentAccount": {
        "id": "ACC-0774-6909",     
        "type": "Client",
        "status": "Active",
        "name": "Ignite Test CDG"
    },
    "audit": {
        "login": {
            "at": "2024-05-09T14:40:28.886Z"
        },
        "created": {
            "at": "2024-05-09T14:40:28.958Z",
            "by": {
                "id": "TKN-7670-9957",
                "href": "/accounts/api-tokens/TKN-7670-9957",
                "name": "[DO NOT REMOVE] PyraProxy"
            }
        },
        "updated": {
            "at": "2024-09-16T12:33:03.761Z",
            "by": {
                "href": "//"
            }
        }
    }
}
```
{% endcode %}
{% endtab %}
{% endtabs %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
