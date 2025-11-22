---
# markdownlint-disable
# vale  off
layout: default
parent: The gym resource
nav_order: 5
# tags used by AI files
description: PUT (replace) the `gym` resource with the specified ID from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites: 
    - /api/gym
related_pages: []
examples: []
api_endpoints: 
    - PUT /gyms/{id}
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# PUT /gym{id}

This action replaces a [`gym`](gym.md) object specified by the `id` parameter of the `gym` resource.
If you only specify one field, the system saves other fields as empty.
This is a good option if you need to change many fields.
If you only want to change one or two fields,
the [PATCH operation](gyms-patch-gym.md) might be a better choice.

## URL

```shell

{server_url}/gyms/{id}
```

## URL parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the `gym` object that you want to change |

## Request headers

This call uses `Content-Type: application/json` for the header.

## Request body

Take a look at the parameters for the request body in the following table.
If you leave any parameters out,
the system creates the entry without it.
The only exception is the ID parameter.
It's already present in URL,
so the system keeps this parameter unless you give it a new one.

| Parameter | Example value | Obligatory |
| ------------- | ----------- | ----------- |
| `lifterId` | 1 | No |
|  `name` | `Iron Temple Barbell Club` | No |
| `description` | `Pending` | No |
|  `location` | `Newark, NJ` | No |
|  `rating` | 5 | No |
|  `id` | 1 | No |

## Example

```js

curl -X PUT "http://localhost:3000/gyms/1" \
  -H "Content-Type: application/json" \
  -d '{
    "lifterId": 1,
    "name": "Iron Temple Barbell Club",
    "description": "Pending.",
    "location": "Newark, NJ",
    "rating": 5,
    "id": 1
    }'
```

Here, `-H` marks the header and `-d` marks the request body.
Backslashes make the code more easily readable.

## Return body

This request returns the new object information.

```js
{
    "lifterId": 1,
    "name": "Iron Temple Barbell Club",
    "description": "Pending.",
    "location": "Newark, NJ",
    "rating": 5,
    "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data changed successfully |
| 404 | Error | Specified record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
