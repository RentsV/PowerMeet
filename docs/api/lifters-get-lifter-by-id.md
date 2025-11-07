---
# markdownlint-disable
# vale  off
layout: default
parent: lifter resource
nav_order: 2
# tags used by AI files
description: GET the `lifter` resource with the specified ID from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites: 
    - /api/lifter
related_pages: []
examples: []
api_endpoints: 
    - GET /lifters
version: "v1.0"
last_updated: "2025-11-07"
# vale  on
# markdownlint-enable
---

# Get a user by ID

Returns a [`lifter`](lifter.md) object specified by the `id` parameter, given that it exists.

## URL

```shell

{server_url}/lifters/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the lifter to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
        "lastName": "Smith",
        "firstName": "Ferdinand",
        "email": "f.smith@example.com",
        "id": 1
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
