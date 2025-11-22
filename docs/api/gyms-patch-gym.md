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

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the gym that you want to change |

## Request information

You don't have to specify the header information.

In the request body, only mention the fields you want to change.
Other fields stay the same.

## Example

```js

curl -X PATCH http://localhost:3000/gyms/5
```

## Return body

This request returns the whole object information with both changed and unchanged fields.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data changed successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
