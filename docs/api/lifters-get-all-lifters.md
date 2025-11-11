---
# markdownlint-disable
# vale  off
layout: default
parent: The lifter resource
nav_order: 1
# tags used by AI files
description: GET all `lifter` resources from the service
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
last_updated: "2025-11-11"
# vale  on
# markdownlint-enable
---

# Get all users

Returns an array of [`lifter`](lifter.md) objects that contains all lifters registered with the service.

## URL

```shell

{server_url}/lifters
```

This call doesn't have any parameters.
It also doesn't need request headers or a request body.
Running this call returns a list of all users.

## Return body

```js
[
    {
        "lastName": "Smith",
        "firstName": "Ferdinand",
        "email": "f.smith@example.com",
        "id": 1
    },
    {
        "lastName": "Jones",
        "firstName": "Jillio",
        "email": "jlo.jones@example.com",
        "id": 2
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
