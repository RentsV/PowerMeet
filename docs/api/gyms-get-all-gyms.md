---
# markdownlint-disable
# vale  off
layout: default
parent: The gym resource
nav_order: 1
# tags used by AI files
description: GET all `gym` resources from the service
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
    - GET /gyms
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# The /gyms endpoint

Running the base endpoint in PowerShell with no method parameter
returns an array of all [`gym`](gym.md) objects.
This contains information about all the gyms registered with the service.

You can read a full tutorial on retrieving this list in Postman [`here`](../tutorials/get-all-gyms.md).
Check out other tutorials to see what else you can do with this resource.

## URL

```shell

{server_url}/gyms
```

This call doesn't have any parameters.
It also doesn't need request headers or a request body in PowerShell.
Running this call returns a list of all gyms.

## Return body

```js
[
    {
        "lifterId": 1,
        "name": "Iron Temple Barbell Club",
        "description": "Powerlifting: combo racks, chalk-friendly policy, calibrated plates.",
        "location": "Newark, NJ",
        "rating": 5,
        "id": 1
        },
    {
        "lifterId": 2,
        "name": "Foundry Strength and Conditioning",
        "description": "Strongman and powerlifting gym with open platform space and deadlift bars.",
        "location": "Jersey City, NJ",
        "rating": 4,
        "id": 2
    },
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
