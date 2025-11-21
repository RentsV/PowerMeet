---
# markdownlint-disable
# vale  off
layout: default
parent: The lifter resource
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
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# The /lifters/{id} endpoint

A `/lifters/{id}` endpoint consists of the base endpoint and an object's ID.
Running this endpoint in PowerShell returns a [`lifter`](lifter.md) object with this ID.
If the specific ID doesn't exist in the system, the system returns a 404 error.

You can read a full tutorial on getting information about a lifter in Postman [`here`](../tutorials/get-a-lifter-by-id.md).
Check out other tutorials to see what else you can do with this resource.

## URL

```shell

{server_url}/lifters/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the lifter to return |

This call doesn't need request headers or a request body.

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
