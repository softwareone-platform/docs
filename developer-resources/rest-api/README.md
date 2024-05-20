# REST API

## Introduction

The **Marketplace Platform REST API** lets you interact with the platform programmatically. Our API is organized around [REST](http://en.wikipedia.org/wiki/Representational\_State\_Transfer), has predictable resource-oriented URLs, uses [JSON-encoded](http://www.json.org/) representations, and uses standard [HTTP response codes](https://en.wikipedia.org/wiki/List\_of\_HTTP\_status\_codes), authentication, and verbs. Use our API to create apps, automate tasks, or build integrations with the platform.&#x20;

## What is a REST API?

An [API](https://en.wikipedia.org/wiki/API) (Application Programming Interface) is a set of rules that allows programs to talk to each other and share data and functions in a standard format over the Internet.

[REST](http://en.wikipedia.org/wiki/Representational\_State\_Transfer) (Representational State Transfer) is a way to design APIs for distributed systems. When people mention a "REST API", they mean an API that uses the HTTP protocol.

These URLs point to different resources, which can be data like JSON, web pages, audio files, or images. You can perform actions on these resources using HTTP methods like GET, POST, PUT, and DELETE:

* **GET** = Retrieve data
* **POST** = Create new data
* **PUT** = Update existing data
* **DELETE** = Remove data

For example, the Marketplace Platform offers several REST APIs for tasks like managing orders and viewing users and accounts. Each API in our platform works similarly, whether you access it directly over HTTP or through helper libraries in various programming languages.

## Authentication

The Marketplace Platform uses [API tokens](../../platform-modules/settings/api-tokens/) to authenticate requests. You can view and manage your API keys in the user interface of your account settings. Include your API token in the "**Authorization**" HTTP header with the "**Bearer**" prefix for authentication.&#x20;

For example, the following request could be used to retrieve a list of Buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas like GitHub or client-side code.

All API requests must be made over **HTTPS**. Calls made over plain HTTP will fail. API requests without authentication will also fail.

## Expected Content Type

The Marketplace Platform API expects the content type of API requests to be "**application/json**" in most cases (except for cases where "multipart/form-data" is used to send attachments)

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
Content-Type: application/json
```

To communicate successfully with the Marketplace Platform APIs, ensure your API requests are formatted using the "**application/json**" content type. Using the wrong content type may result in unexpected behavior or errors.

## Base API Endpoint

The base endpoint for the Marketplace Platform API is:

```
https://api.platform.softwareone.com/public
```

&#x20;All API requests start from that base URL. For example, if you have an endpoint like:

```
/v1/accounts/buyers
```

The fully qualified URL that you need to use is:

```
https://api.platform.softwareone.com/public/v1/accounts/buyers
```

&#x20;Use this base endpoint with specific API paths to correctly access the resources and services provided by the Marketplace Platform.

## Explore the APIs <a href="#explore-the-apis" id="explore-the-apis"></a>

{% content-ref url="accounts-api/" %}
[accounts-api](accounts-api/)
{% endcontent-ref %}

{% content-ref url="commerce-api/" %}
[commerce-api](commerce-api/)
{% endcontent-ref %}

{% content-ref url="catalog-api/" %}
[catalog-api](catalog-api/)
{% endcontent-ref %}
