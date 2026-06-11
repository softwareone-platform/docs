# Certificate

A certificate is issued to a client or partner as confirmation that they meet a specific program's requirements. This document is proof that the client or partner has adhered to the vendor's standards and is now eligible to purchase or access their products.&#x20;

The following rules apply to certificates:

* A certificate can only be created or re-enrolled for published programs.
* A client or partner can re-enroll for a certificate if it's in **Active** or **Expired** status. Re-enrollment is not permitted for terminated certificates.
* A certificate can automatically expire on its expiration date, changing its status to **Expired**.

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="234">Field</th><th width="125">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string, <a data-footnote-ref href="#user-content-fn-1">core</a></td><td>(Read-only) The business identifier of the certificate. </td></tr><tr><td><code>href</code></td><td>string, core</td><td>(Read-only) The resource URI of the certificate.</td></tr><tr><td><code>program</code></td><td>object, core</td><td><p>Represents the <a href="../program/"><code>program</code></a> to which this certificate applies. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "PRG-1234-5678",
    "href": "/program/programs/PRG-1234-5678",
    "name": "Microsoft AI Cloud Partner"
}
</code></pre></td></tr><tr><td><code>client</code></td><td>object</td><td>Represents the client or partner <a href="../../accounts-api/account/"><code>account</code></a> object to which the certificate belongs. </td></tr><tr><td><code>applicableTo</code></td><td>string, core</td><td>The scope in which the given enrollment is created. Allowed values are <code>buyer</code> or <code>licensee</code>.</td></tr><tr><td><code>buyer</code></td><td>object, core</td><td>(Optional) Represents the <a href="../../accounts-api/buyer/"><code>buyer</code></a> object, if the enrollment applies to the buyer. </td></tr><tr><td><code>licensee</code></td><td>object, core </td><td><p>(Optional) Represents the <a href="../../accounts-api/licensee/"><code>licensee</code></a> object if the enrollment applies to the licensee. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
    "id": "CER-1234-1234",
    "href": "v1/accounts/licensees/LIC-1234-1234-1234"
    "name": "Stark Canada Limited",
    "externalId": "WW-CON-12345678"
}
</code></pre></td></tr><tr><td><code>eligibility</code></td><td>eligibility, core</td><td><p>Configuration of the partner program.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "client": true,
  "partner": false
}
</code></pre></td></tr><tr><td><code>externalIds</code></td><td>object</td><td><p>Represents the <a href="../../../api-usage-and-reference/common-api-objects/externalids.md">externalIds</a> object, containing the identifier for the external system.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{
  "vendor": "ven-1233-3222"
}
</code></pre></td></tr><tr><td><code>status</code></td><td>enum, core</td><td><p>(Read-only) The certificate's status. Allowed values are:</p><ul><li><code>Pending</code></li><li><code>Updating</code></li><li><code>Active</code></li><li><code>Terminated</code></li><li><code>Expired</code></li></ul></td></tr><tr><td><code>statusNotes</code></td><td>string</td><td>(Optional) Notes provided by the vendor to terminate a certificate.</td></tr><tr><td><code>expirationDate</code></td><td>dateTime</td><td>(Optional) The expiration date of the certificate. When the date has passed, the system expires the certificate. </td></tr><tr><td><code>template</code></td><td>object</td><td><p>(Optional) Represents the <a href="../../catalog-api/templates/"><code>template</code></a> object.</p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">{ 
  "id": "PTP-1234-4444", 
  "href": "/programs/PRG-1234 1234/templates/TPP-1234-4444",
  "name": "Successful Activation" 
}
</code></pre></td></tr><tr><td><code>parameters.fulfillment</code></td><td>object</td><td><p>Represents the <a href="../enrollment/#enrollment-parameter"><code>orderParameter</code></a> object, which holds a definition of a parameter, its value, and associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tenant Id",
      "externalId": "tenant_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }
]
</code></pre></td></tr><tr><td><code>parameters.ordering</code></td><td>object</td><td><p>Represents the <a href="../enrollment/#enrollment-parameter"><code>orderParameter</code></a> object, which contains a definition of a parameter, its value, and associated errors. </p><p>Example:</p><pre class="language-json" data-overflow="wrap" data-line-numbers data-full-width="true"><code class="lang-json">[
  {
      "id": "PRM-1234-1234-1234",
      "name": "Tenant Id",
      "externalId": "tenant_id",
      "constraints": {
          "readonly": false,
          "hidden": true,
          "required": true,
          "unique": false
      },
      "value": "69b73824-ce76-4866-ad47-b615ae9d8998",
      "error": {
          "id": "E001234",
          "message": "Incorrect parameter value"
      }
  }
]
</code></pre></td></tr><tr><td><code>audit</code></td><td>object</td><td>(Read-only) Represents the <a href="../../../api-usage-and-reference/common-api-objects/audit.md"><code>audit</code></a> object. </td></tr></tbody></table>

## Parameter value <a href="#parametervalue" id="parametervalue"></a>

{% include "../../../../.gitbook/includes/api-table-header.md" %}

<table><thead><tr><th width="142">Field</th><th width="112">Type</th><th>Description</th></tr></thead><tbody><tr><td><code>id</code></td><td>string</td><td>The identifier of the parameter definition this value refers to. </td></tr><tr><td><code>externalId</code></td><td>string</td><td>The ID of the parameter in the external system. </td></tr><tr><td><code>type</code></td><td>string</td><td>The type of the parameter definition. </td></tr><tr><td><code>name</code></td><td>string</td><td>The display name of the parameter. </td></tr><tr><td><code>value</code></td><td>string</td><td>The value of the parameter. </td></tr></tbody></table>

## Example

{% code title="CERTIFICATE OBJECT" overflow="wrap" lineNumbers="true" %}
```json
{
    "id": "CER-1495-4162-8138",
    "name": "Certainly a certificate",
    "revision": 1,
    "program": {
        "id": "PRG-8803-8286",
        "name": "Microsoft2 AI Cloud Friend",
        "revision": 2,
        "icon": "/v1/program/programs/PRG-8803-8286/icon",
        "status": "Unpublished",
        "applicableTo": "Licensee",
        "products": [
            {
                "id": "PRD-0262-5461",
                "name": "Don't touch it - testing in progress",
                "icon": "/v1/catalog/products/PRD-0262-5461/icon",
                "revision": 2,
                "externalIds": {},
                "status": "Published"
            },
            {
                "id": "PRD-0506-8226",
                "name": "iProduct",
                "icon": "/v1/catalog/products/PRD-0506-8226/icon",
                "revision": 2,
                "externalIds": {
                    "operations": "12345"
                },
                "status": "Published"
            },
            {
                "id": "PRD-1126-6342",
                "name": "ProFour",
                "icon": "/v1/catalog/products/PRD-1126-6342/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-1186-8657",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-1186-8657/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-1324-5809",
                "name": "Test",
                "icon": "/v1/catalog/products/PRD-1324-5809/icon",
                "revision": 1,
                "externalIds": {
                    "operations": "1666"
                },
                "status": "Pending"
            },
            {
                "id": "PRD-1361-4823",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-1361-4823/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-1458-4448",
                "name": "ProOne",
                "icon": "/v1/catalog/products/PRD-1458-4448/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Published"
            },
            {
                "id": "PRD-1503-5649",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-1503-5649/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-1695-6569",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-1695-6569/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-1712-6041",
                "name": "This is another product",
                "icon": "/v1/catalog/products/PRD-1712-6041/icon",
                "revision": 31,
                "externalIds": {},
                "status": "Published"
            },
            {
                "id": "PRD-2370-3582",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-2370-3582/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-2599-3780",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-2599-3780/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-2876-3270",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-2876-3270/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-3035-5906",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-3035-5906/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-3225-9621",
                "name": "Adobius Agobius",
                "icon": "/v1/catalog/products/PRD-3225-9621/icon",
                "revision": 4,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-4087-9832",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-4087-9832/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-4113-0835",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-4113-0835/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-4358-5858",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-4358-5858/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-4438-6974",
                "name": "Producto estupendo",
                "icon": "/v1/catalog/products/PRD-4438-6974/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Published"
            },
            {
                "id": "PRD-4584-0141",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-4584-0141/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-5008-6643",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-5008-6643/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-5423-8617",
                "name": "Release 009",
                "icon": "/v1/catalog/products/PRD-5423-8617/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-5469-4797",
                "name": "Price List Items Test product",
                "icon": "/v1/catalog/products/PRD-5469-4797/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-5486-6163",
                "name": "Adobe Bo",
                "icon": "/v1/catalog/products/PRD-5486-6163/icon",
                "revision": 43,
                "externalIds": {
                    "operations": "03543356356356365",
                    "defaultErpItem": "879878"
                },
                "status": "Published"
            },
            {
                "id": "PRD-5624-3062",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-5624-3062/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-5636-4901",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-5636-4901/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-6435-6769",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-6435-6769/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-6478-2097",
                "name": "AutomatedTajfunPending",
                "icon": "/v1/catalog/products/PRD-6478-2097/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-6847-2813",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-6847-2813/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-6998-2587",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-6998-2587/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-7070-4351",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-7070-4351/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-7162-5819",
                "name": "ProTwo",
                "icon": "/v1/catalog/products/PRD-7162-5819/icon",
                "revision": 3,
                "externalIds": {},
                "status": "Published"
            },
            {
                "id": "PRD-7399-8133",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-7399-8133/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-7492-6453",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-7492-6453/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-7622-1820",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-7622-1820/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-7811-7846",
                "name": "Tajfun",
                "icon": "/v1/catalog/products/PRD-7811-7846/icon",
                "revision": 3,
                "externalIds": {
                    "operations": "1234567890"
                },
                "status": "Published"
            },
            {
                "id": "PRD-8265-6648",
                "name": "BluewindPro",
                "icon": "/v1/catalog/products/PRD-8265-6648/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-8289-7768",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-8289-7768/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-8557-8571",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-8557-8571/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-8599-9806",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-8599-9806/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-8674-3473",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-8674-3473/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-8854-4878",
                "name": "AutomatedTajfunUnpublished",
                "icon": "/v1/catalog/products/PRD-8854-4878/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Published"
            },
            {
                "id": "PRD-8854-7061",
                "name": "AutomatedTajfunPublished",
                "icon": "/v1/catalog/products/PRD-8854-7061/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Unpublished"
            },
            {
                "id": "PRD-9298-0552",
                "name": "ProThree",
                "icon": "/v1/catalog/products/PRD-9298-0552/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            },
            {
                "id": "PRD-9689-6324",
                "name": "Product with mad quantity of Terms",
                "icon": "/v1/catalog/products/PRD-9689-6324/icon",
                "revision": 1,
                "externalIds": {
                    "operations": "IAMD3FAULT"
                },
                "status": "Unpublished"
            },
            {
                "id": "PRD-9920-1302",
                "name": "MPT_QA_Product",
                "icon": "/v1/catalog/products/PRD-9920-1302/icon",
                "revision": 1,
                "externalIds": {},
                "status": "Pending"
            }
        ]
    },
    "vendor": {
        "id": "ACC-1762-8332",
        "name": "Test Tajfun Vendor",
        "icon": "/v1/accounts/accounts/ACC-1762-8332/icon",
        "revision": 8,
        "type": "Vendor",
        "status": "Enabled"
    },
    "externalIds": {},
    "client": {
        "id": "ACC-7843-4996",
        "name": "Experimental Client #37",
        "revision": 1,
        "type": "Client",
        "status": "Active"
    },
    "applicableTo": "Licensee",
    "licensee": {
        "id": "LCE-2722-7432-2049",
        "name": "US Licensee",
        "revision": 1
    },
    "eligibility": {
        "client": true,
        "partner": true
    },
    "status": "Terminated",
    "statusNotes": "this certificate needs to be terminated",
    "expirationDate": "2025-01-31",
    "parameters": {
        "ordering": [],
        "fulfillment": []
    },
    "audit": {
        "terminated": {
            "at": "2025-03-27T20:19:21.004Z",
            "by": {
                "id": "USR-0000-0032",
                "name": "Mariya Surovtseva",
                "revision": 1
            }
        },
        "created": {
            "at": "2025-02-03T10:52:56.814Z",
            "by": {
                "id": "USR-0000-0032",
                "name": "Mariya Surovtseva",
                "revision": 1
            }
        },
        "updated": {
            "at": "2025-04-25T16:45:51.902Z",
            "by": {
                "id": "USR-0000-0037",
                "name": "Michael Saunders",
                "revision": 1
            }
        }
    }
}
```
{% endcode %}

[^1]: **Core** indicates the field is part of the base object schema. This is not the same as “required”.
