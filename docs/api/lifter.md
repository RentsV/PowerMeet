---
# markdownlint-disable
# vale  off
layout: default
nav_order: 4
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `lifter` resource"
tags: 
    - api
categories:
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/add-a-new-lifter
examples: []
api_endpoints: 
    - /lifters
    - /lifters{id}
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# The `lifter` resource

Base endpoint:

```shell

{server_url}/lifters
```

Contains information about the lifters of the service.

A `lifter` resource describes the users associated with the gyms.
Before you can create a `gym` resource in the service,
you must create the `lifter` resource to assign to this `gym`.

To find out more about the gym-related information instead, 
read the [`gym` resource page](gym.md).

## Resource properties

Sample `lifter` resource

```js

{
    "lastName": "Smith",
    "firstName": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `lastName` | string | The lifter's last name |
| `firstName` | string | The lifter's first name |
| `email` | string | The lifter's email address |
| `id` | number | The lifter's unique record ID |

## Available operations

* [GET /lifters](lifters-get-all-lifters.md)
* [GET /lifters{id}](lifters-get-lifter-by-id.md)
* [POST /lifters](lifters-post-lifter.md)
* [PATCH /lifters{id}](lifters-patch-lifter.md)
* [PUT /lifters{id}](lifters-put-lifter.md)
* [DELETE /lifters{id}](lifters-delete-lifter-by-id.md)
