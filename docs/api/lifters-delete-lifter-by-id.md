---
# markdownlint-disable
# vale  off
layout: default
parent: The lifter resource
nav_order: 6
# tags used by AI files
description: DELETE the `lifter` resource with the specified ID from the service
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
    - DELETE /lifters/{id}
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# DELETE /lifters{id}

This action deletes a [`lifter`](lifter.md) specified by the `id` parameter of the `lifter` resource.

## URL

```shell

{server_url}/lifters/{id}
```

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the lifter that you want to delete |

## Request information

You don't have to specify the header information and this request has no request body.

This call also has no return body, no matter if the call is successful or not.
The system shows the return status, either 200 or 404.
200 means that the deletion was successful,
404 means that it failed.

## Example

```js

curl -X DELETE "http://localhost:3000/lifters/3"
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data deleted successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
