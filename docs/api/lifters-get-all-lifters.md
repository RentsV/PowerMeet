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

# The /lifters endpoint

Running the base endpoint in PowerShell with no method parameter
returns a list of all [`lifter`](lifter.md) objects.
It contains information about all the lifters registered with the service.

You can read a full tutorial on receiving this list in Postman [`here`](../tutorials/get-all-lifters.md).
Check out other tutorials to see what else you can do with this resource.

## URL

```shell

{server_url}/lifters
```

This call doesn't have any parameters.
It also doesn't need request headers or a request body in PowerShell.
Running this call returns a list of all users.

## Return body

```js
[
    {
        "lastName": "Johnson",
        "firstName": "Tara",
        "email": "tara.johnson@example.com",
        "id": 1
    },
    {
        "lastName": "Nguyen",
        "firstName": "Chris",
        "email": "chris.nguyen@example.com",
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
