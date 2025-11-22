---
# markdownlint-disable
# vale  off
layout: default
parent: The lifter resource
nav_order: 4
# tags used by AI files
description: PATCH the `lifter` resource with the specified ID from the service
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
    - PATCH /lifters/{id}
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# PATCH /lifter{id}

This action changes a [`lifter`](lifter.md) object specified by the `id` parameter of the `lifter` resource.

## URL

```shell

{server_url}/lifters/{id}
```

## URL parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | ID of the lifter that you want to change |

## Request headers

This call uses `Content-Type: application/json` for the header.

## Request body

Take a look at the parameters for the request body in the following table.
If you leave any parameters out,
the system won't change them.

| Parameter | Example value | Obligatory |
| ------------- | ----------- | ----------- |
| `lastName` | `Johnson` | No |
|  `firstName` | `Tara` | No |
| `email` | `tara24.johnson@example.com` | No |
|  `id` | 1 | No |

## Example

```js

curl -X PATCH "http://localhost:3000/lifters/1" \
  -H "Content-Type: application/json" \
  -d '{
    "email": "tara.newemail@example.com"
    }'
```

Here, `-H` marks the header and `-d` marks the request body.
Backslashes make the code more easily readable.

## Return body

This request returns the whole object information with both changed and unchanged fields.

```js
{
    "lastName": "Johnson",
    "firstName": "Tara",
    "email": "tara.newemail@example.com",
    "id": 1
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data changed successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
