---
# markdownlint-disable
# vale  off
layout: default
parent: The lifter resource
nav_order: 3
# tags used by AI files
description: POST a new `lifter` resource
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
    - POST /lifters
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# POST /lifters

Running the base endpoint in PowerShell with a PUT method adds a new [`lifter`](lifter.md) object.

You can read a full tutorial on adding a new lifter in Postman [`here`](../tutorials/add-a-new-lifter.md).

## URL

```shell

{server_url}/lifters
```

## Request information

This call doesn't have any parameters.
You need to specify the fields in the request body,
otherwise it creates a `lifter` object with only an ID.

## Example

```js

curl -X POST http://localhost:3000/lifters
```


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
| 200 | Success | Requested data added successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
