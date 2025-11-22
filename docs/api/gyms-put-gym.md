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

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the `gym` object that you want to change |

## Request information

You don't have to specify the header information.

In the request body, write out all the fields.
As this operation replaces the whole object,
the system saves the fields you don't mention as empty.

## Example

```js

curl -X PUT http://localhost:3000/gyms/5
```

## Return body

This request returns the new object information.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data changed successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
