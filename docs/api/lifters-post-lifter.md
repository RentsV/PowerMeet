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

## Request headers

This call uses `Content-Type: application/json` for the header.

## Request body

Take a look at the parameters for the request body in the following table.
If you leave any parameters out,
the system creates the entry without it.
The only exception is the ID parameter.
If you don't give an ID value, the system assigns an ID value itself.

| Parameter | Example value | Obligatory |
| ------------- | ----------- | ----------- |
| `lastName` | `Torvalds` | No |
|  `firstName` | `Linus` | No |
| `email` | `linus.torvalds@example.com` | No |
|  `id` | 5 | No |

## Example

```js

curl -X POST "http://localhost:3000/lifters" \
  -H "Content-Type: application/json" \
  -d '{
    "lastName": "Torvalds",
    "firstName": "Linus",
    "email": "linus.torvalds@example.com"
    }'
```

Here, `-H` marks the header and `-d` marks the request body.
Backslashes make the code more easily readable.

## Return body

```js
{
    "lastName": "Torvalds",
    "firstName": "Linus",
    "email": "linus.torvalds@example.com",
    "id": 5
},
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data added successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
