---
description: >-
  Resource Query Language (RQL) is a query language that Marketplace Platform
  uses in the REST API.
---

# Resource Query Language

## Introduction

The **Resource Query Language** (or **RQL**) is used for querying and manipulating resources in the Marketplace Platform's [REST API](./). With RQL, you can filter, sort, paginate, and project data. It is simple to use but flexible enough to handle complex scenarios.

## Using RQL&#x20;

RQL consists of a set of operators that can be classified into three main categories:

1. **Comparison Operators**: These perform comparisons like equals, greater than, etc.
2. **Logical Operators**: These combine multiple conditions.
3. **Algorithmic Operators**: These handle functionalities like sorting and pagination.

Operators are formatted as `operator(arg1,arg2,...)`. Complex expressions can be created by nesting these operators.

## Practical Examples

Suppose you want to list all users with a specific domain. Implementing filtering is essential, and this is where RQL comes in.

### **Basic Filtering**

To display all users with the first name "Buzz", your GET request would look like this:

```
GET /v1/accounts/users?eq(firstName,Buzz)
```

### Sorting

To sort users based on their first name, your GET request would look like this:

```
GET /v1/accounts/users?order=firstName
```

To sort in the opposite direction, the '-' operator can be used:

```
GET /v1/accounts/users?order=-firstName
```

### Pagination

To paginate your results with a limit of 10 users and to retrieve the third page (offset 20):

```
GET /v1/accounts/users?limit=10&offset=20
```

* The first parameter `limit=10` expresses the number of users to return
* Second parameter offset=`20` offsets the starting position in the result set. The first 20 users will be skipped.

### Projection

To request specific fields, such as `forstName`, `lastName`, and `email` to be included, the `select=+` operator can be used:

```
GET /v1/accounts/users?select=+firstName,+lastName,+email
```

To request certain fields to be excluded, the `select=-` operator can be used:

```
GET /v1/accounts/users?select=-firstName,-lastName,-email
```

### Search

To search for all users with the firstName starting from 'Bu', the following query can be used:

```
GET /v1/accounts/users?ilike(firstName,Bu*)
```

the operator `ilike` performs a case-insensitive search.

### Combining Operators

Logical operators can be used to combine multiple operators. For example, to filter users with first name "Buzz" and last name "Astral":

```
GET GET /v1/accounts/users?and(eq(firstName,Buzz),eq(lastName,Astral))
```

## Operators

<table><thead><tr><th width="341">Function</th><th>Description</th></tr></thead><tbody><tr><td><strong>or</strong> (&#x3C;condition1>, &#x3C;condition2>, ...)</td><td>Returns records that satisfy at least one of the specified conditions.</td></tr><tr><td><strong>and</strong> (&#x3C;condition1>, &#x3C;condition2>, ...)</td><td>Returns records that satisfy all of the specified conditions.</td></tr><tr><td><strong>not</strong> (&#x3C;condition>)</td><td>Returns records that do not satisfy the specified condition.</td></tr><tr><td><strong>empty</strong> ( )</td><td>Constant that is used to represent an empty string. Example: /users?firstName=empty()</td></tr><tr><td><strong>order</strong> = +&#x3C;property1>,-&#x3C;property2>, ...</td><td>Sorts the returned records by <code>&#x3C;property></code>. <code>+</code>represents the ascending order, while <code>-</code>represents the descending order.</td></tr><tr><td><strong>select</strong> = +&#x3C;property1>, -&#x3C;property2>, ...</td><td>Used to add and remove certain objects from the representation.</td></tr><tr><td><strong>offset</strong> = &#x3C;value></td><td>Offsets the starting position in the resulting set.</td></tr><tr><td><strong>limit</strong> = &#x3C;value></td><td>Limits the number of returned records by the specified value.</td></tr><tr><td><strong>eq</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> exactly matches the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ne</strong>  (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> does not match the <code>&#x3C;value></code>.</td></tr><tr><td><strong>gt</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is greater than the <code>&#x3C;value></code>.</td></tr><tr><td><strong>ge</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is greater or equal to the <code>&#x3C;value></code>.</td></tr><tr><td><strong>lt</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is less than the <code>&#x3C;value></code>.</td></tr><tr><td><strong>le</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> is less than or equal to the <code>&#x3C;value></code>.</td></tr><tr><td><strong>like</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> contains <code>&#x3C;value></code> as as substring.</td></tr><tr><td><strong>ilike</strong> (&#x3C;property>, &#x3C;value>)</td><td>Filters records where <code>&#x3C;property></code> contains <code>&#x3C;value></code> as as substring.</td></tr><tr><td><strong>in</strong> (&#x3C;property>,(&#x3C;value1>,&#x3C;value2>,...))</td><td>Filters records where <code>&#x3C;property></code> matches any of the listed <code>&#x3C;value>s</code>.</td></tr><tr><td>out (&#x3C;property>,(&#x3C;value1>,&#x3C;value2>,...))</td><td>Filters records where <code>&#x3C;property></code> matches none of the listed <code>&#x3C;value>s</code>.</td></tr><tr><td>any (&#x3C;collection>, &#x3C;condition>)</td><td>Filters records by applying <code>&#x3C;condition></code> to the nested <code>&#x3C;collection></code> .</td></tr><tr><td>all (&#x3C;collection>, &#x3C;condition>)</td><td>Filters records by applying <code>&#x3C;condition></code> to the nested <code>&#x3C;collection></code> .</td></tr></tbody></table>
