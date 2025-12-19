---
description: Learn about Resource Query Language and how to use it.
---

# Resource Query Language

Resource Query Language (RQL) is a query language used by the Marketplace Platform in its REST API. It's used for querying and manipulating resources in the Marketplace Platform's [REST API](./).&#x20;

With RQL, you can filter, sort, paginate, and project data. It's simple to use but flexible enough to handle complex scenarios.

## Using RQL&#x20;

RQL consists of a set of operators that can be classified into three main categories:

* **Comparison operators** - These operators perform comparisons like equals, greater than, and so on.
* **Logical operators** - These operators combine multiple conditions.
* **Algorithmic operators** - These operators handle functionalities, like sorting and pagination.

Operators are formatted as `operator(arg1,arg2,...)`. Complex expressions can be created by nesting these operators.

## Practical examples

Let's say you want to list all users with a specific domain. Implementing filtering is essential, and this is where RQL comes in.

### **Basic filtering**

To display all users with the first name 'Buzz, your `GET` request will look like this:

```http
GET /v1/accounts/users?firstName=Buzz
```

The same expression can be written as:&#x20;

```http
GET /v1/accounts/users?eq(firstName,Buzz)
```

### Sorting

To sort users based on their first name, your `GET` request will look like this:

```http
GET /v1/accounts/users?order=firstName
```

To sort in the opposite direction, the '-' operator can be used:

```http
GET /v1/accounts/users?order=-firstName
```

### Pagination

To paginate your results with a limit of 10 users and to retrieve the third page (offset 20):

```http
GET /v1/accounts/users?limit=10&offset=20
```

* The first parameter `limit=10` expresses the number of users to return
* The second parameter `offset=20` offsets the starting position in the result set. The first 20 users will be skipped.

### Projection

To request specific fields, such as `firstName`, `lastName`, and `email` to be included, the `select=+` operator can be used:

```http
GET /v1/accounts/users?select=+firstName,+lastName,+email
```

To request certain fields to be excluded, the `select=-` operator can be used:

```http
GET /v1/accounts/users?select=-firstName,-lastName,-email
```

### Search

To search for all users with the first name starting from 'Bu', the following query can be used:

```http
GET /v1/accounts/users?ilike(firstName,Bu*)
```

the operator `ilike` performs a case-insensitive search.

### Combining operators

Logical operators can be used to combine multiple operators. For example, to filter users with first name 'Buzz' and last name 'Astral':

```http
GET /v1/accounts/users?and(eq(firstName,Buzz),eq(lastName,Astral))
```

In simple cases, a combined expression can also be written in the following form:

```http
GET /v1/accounts/users?firstName=Buzz&lastName=Astral
```

## Operators

<table><thead><tr><th width="341">Function</th><th>Description</th></tr></thead><tbody><tr><td><strong>or</strong> (&#x3C;condition1>, &#x3C;condition2>, ...)</td><td>Returns records that satisfy at least one of the specified conditions.</td></tr><tr><td><strong>and</strong> (&#x3C;condition1>, &#x3C;condition2>, ...)</td><td>Returns records that satisfy all of the specified conditions.</td></tr><tr><td><strong>not</strong> (&#x3C;condition>)</td><td>Returns records that do not satisfy the specified condition.</td></tr><tr><td><strong>empty</strong> ( )</td><td>Constant that is used to represent an empty string. Example: /users?firstName=empty()</td></tr><tr><td><strong>null</strong> ( )</td><td>Constant that is used to represent an unassigned ("null") value. Example: /users?firstName=null()</td></tr><tr><td><strong>order</strong> = +&#x3C;property1>,-&#x3C;property2>, ...</td><td>Sorts the returned records by <code>&#x3C;property></code>. <code>+</code> represents the ascending order, while <code>-</code> represents the descending order.</td></tr><tr><td><strong>select</strong> = +&#x3C;property1>, -&#x3C;property2>, ...</td><td>Used to add and remove certain objects from the representation.</td></tr><tr><td><strong>offset</strong> = &#x3C;value></td><td>Offsets the starting position in the resulting set.</td></tr><tr><td><strong>limit</strong> = &#x3C;value></td><td>Limits the number of returned records by the specified value.</td></tr><tr><td><strong>eq</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> exactly matches the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ne</strong>  (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> does not match the <code>&#x3C;value></code>.</td></tr><tr><td><strong>gt</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is greater than the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ge</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is greater or equal to the <code>&#x3C;value></code>.</td></tr><tr><td><strong>lt</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is less than the <code>&#x3C;value></code>.</td></tr><tr><td><strong>le</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is less than or equal to the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ilike</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> contains <code>&#x3C;value></code> as a substring, the comparison is case-insensitive.</td></tr><tr><td><strong>in</strong> (&#x3C;property>,(&#x3C;value1>,&#x3C;value2>,...))</td><td>Filters records where <code>&#x3C;property></code> matches any of the listed <code>&#x3C;value>s</code>.</td></tr><tr><td><strong>out</strong> (&#x3C;property>,(&#x3C;value1>,&#x3C;value2>,...))</td><td>Filters records where <code>&#x3C;property></code> matches none of the listed <code>&#x3C;value>s</code>.</td></tr><tr><td><strong>any</strong> (&#x3C;collection>, &#x3C;condition>)</td><td>Filters records by applying <code>&#x3C;condition></code> to the nested <code>&#x3C;collection></code> .</td></tr><tr><td><strong>all</strong> (&#x3C;collection>, &#x3C;condition>)</td><td>Filters records by applying <code>&#x3C;condition></code> to the nested <code>&#x3C;collection></code> .</td></tr></tbody></table>

## Advanced use cases <a href="#markdown-header-more-information" id="markdown-header-more-information"></a>

### Special characters in values

To pass special characters (like, &^$?) or whitespaces as values to RQL operators, enclose them in either double quotes (") or single quotes (') as shown in the following example:

```http
GET /v1/accounts/users?firstName="Buzz !!!"
```

If you need to include a quotation mark within the value, you can do so by enclosing it with a different type of quotation mark, as shown in the following example:

```http
GET /v1/accounts/users?firstName="Buzz with the ' Quote"
```

Allowing you to pass these special symbols as values.

### The asterisk Character and the ilike operator

The asterisk (\*) character has a special meaning in the `ilike` operator, matching zero or more characters in its place from the parameter value. For example, the "\*dog" pattern will match strings like "big dog" and "dog," but it will not match "big dog!" because of the exclamation mark.

If you need to use the asterisk (\*) character itself in the pattern, you can escape it as '\*', as shown in the following example:

```http
GET /v1/accounts/users?ilike(firstName,"The\**")
```

The ilike operator in this case will be searching for the literal value “The\*” at the beginning of the firstName property.

## Further resources <a href="#further-resources" id="further-resources"></a>

For a C# reference implementation of RQL for .NET applications, see the GitHub repository at [https://github.com/softwareone-platform/mpt-rql-net](https://github.com/softwareone-platform/mpt-rql-net).
