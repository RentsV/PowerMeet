---
# markdownlint-disable
# vale  off
layout: default
parent: The gym resource
nav_order: 2
# tags used by AI files
description: DELETE the `gym` resource with the specified ID from the service
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
    - DELETE /gyms/{id}
version: "v1.0"
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# GET /gyms/{id}

A `/gyms/{id}` endpoint consists of the base endpoint and an object's ID.
Running this endpoint in PowerShell returns a [`gym`](gym.md) object with this ID.
If the specific ID doesn't exist in the system, the system returns a 404 error.

You can read a full tutorial on getting information about a gym in Postman [`here`](../tutorials/get-a-gym-by-id.md).
Check out other tutorials to see what else you can do with this resource.

## URL

```shell

{server_url}/gyms/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the gym |

This call doesn't need request headers or a request body.

## Return body

```js
{
    "lifterId": 2,
    "name": "Foundry Strength and Conditioning",
    "description": "Strongman and powerlifting gym with open platform space and deadlift bars.",
    "location": "Jersey City, NJ",
    "rating": 4,
    "id": 2
}

```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified gym record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
