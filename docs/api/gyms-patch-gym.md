---
# markdownlint-disable
# vale  off
layout: default
parent: The gym resource
nav_order: 4
# tags used by AI files
description: PATCH the `gym` resource with the specified ID from the service
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
    - PATCH /gyms/{id}
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# PATCH /gym{id}

This action changes a [`gym`](gym.md) object specified by the `id` parameter of the `gym` resource.

## URL

```shell

{server_url}/gyms/{id}
```

## URL parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the gym that you want to change |

## Request headers

This call uses `Content-Type: application/json` for the header.

## Request body

Take a look at the parameters for the request body in the following table.
If you leave any parameters out,
the system won't change them.

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

curl -X PATCH "http://localhost:3000/gyms/1" \
  -H "Content-Type: application/json" \
  -d '{
    "rating": 4,
    "description": "Slightly less chalk-friendly now."
    }'
```

Here, `-H` marks the header and `-d` marks the request body.
Backslashes make the code more easily readable.

## Return body

This request returns the whole object information with both changed and unchanged fields.

```js
{
    "lifterId": 1,
    "name": "Iron Temple Barbell Club",
    "description": "Slightly less chalk-friendly now.",
    "location": "Newark, NJ",
    "rating": 4,
    "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data changed successfully |
| 404 | Error | Specified record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
