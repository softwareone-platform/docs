# REST API

## Introduction

The **Marketplace Platform REST API** lets you interact with the platform programmatically. Our API is organized around [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer), has predictable resource-oriented URLs, uses [JSON-encoded](http://www.json.org/) representations, and uses standard [HTTP response codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes), authentication, and verbs. Use our API to create apps, automate tasks, or build integrations with the platform.&#x20;

## Beginners guide

{% embed url="https://www.youtube.com/watch?v=0NF8OtCA-kU" %}
Video tutorial: REST APIs for Beginners
{% endembed %}

## What is a REST API?

An Application Programming Interface ([API](https://en.wikipedia.org/wiki/API)) is a set of rules that allows programs to talk to each other and share data and functions in a standard format over the Internet.

Representational State Transfer ([REST](http://en.wikipedia.org/wiki/Representational_State_Transfer)) is a way to design APIs for distributed systems. When people mention a REST API, they mean an API that uses the HTTP protocol.

These URLs point to different resources, which can be data like JSON, web pages, audio files, or images. You can perform actions on these resources using HTTP methods like GET, POST, PUT, and DELETE:

* **GET** = Retrieve data
* **POST** = Create new data
* **PUT** = Update existing data
* **DELETE** = Remove data

For example, the Marketplace Platform offers several REST APIs for tasks like managing orders and viewing users and accounts. Each API in our platform works similarly, whether you access it directly over HTTP or through helper libraries in various programming languages.

## Authentication

The Marketplace Platform uses [API tokens](../../modules-and-features/settings/api-tokens/) to authenticate requests. You can view and manage your API keys in the user interface of your account settings. Include your API token in the '**Authorization'** HTTP header with the '**Bearer**' prefix for authentication.&#x20;

For example, the following request could be used to retrieve a list of buyers:

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
```

Your API keys have permissions assigned to them, so keep them secure. Do not share your secret API keys in public areas like GitHub or client-side code.

All API requests must be made over **HTTPS**. Calls made over plain HTTP will fail. API requests without authentication will also fail.

## Content type

The Marketplace Platform API expects the **content type** of API requests to be '**application/json**' in most cases (except for cases where 'multipart/form-data' is used to send attachments)

```http
GET https://api.platform.softwareone.com/public/v1/accounts/buyers
Authorization: Bearer {TOKEN_VALUE}
Content-Type: application/json
```

To communicate successfully with the Marketplace Platform APIs, ensure your API requests are formatted using the '**application/json**' content type. Using the wrong content type can result in unexpected behavior or errors.

## API endpoint

The base endpoint for the Marketplace Platform API is:

```http
https://api.platform.softwareone.com/public
```

&#x20;All API requests start from that base URL. For example, if you have an endpoint like:

```http
/v1/accounts/buyers
```

The fully qualified URL that you need to use is:

```http
https://api.platform.softwareone.com/public/v1/accounts/buyers
```

Use this base endpoint with specific API paths to correctly access the resources and services provided by the Marketplace Platform.

## Resource Query Language

The **Resource Query Language** (**RQL**) is used for querying and manipulating resources in the Marketplace Platform's APIs. With RQL, you can filter, sort, paginate, and project data. It is simple to use but flexible enough to handle complex scenarios.

For example, to display all users with the first name 'Buzz', your `GET` request will look like this:

```http
GET /v1/accounts/users?firstName=Buzz
```

See [Resource Query Language](resource-query-language.md) for more details.

## Errors handling <a href="#explore-the-apis" id="explore-the-apis"></a>

Our platform reports errors using HTTP status codes in a standard format, ensuring consistency and clarity. For more details, see [Errors Handling](errors-handling.md).

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

{% content-ref url="notifications-api/" %}
[notifications-api](notifications-api/)
{% endcontent-ref %}
