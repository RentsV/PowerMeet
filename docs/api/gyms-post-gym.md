---
# markdownlint-disable
# vale  off
layout: default
parent: The gym resource
nav_order: 3
# tags used by AI files
description: POST a new `gym` resource
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
    - POST /gyms
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# POST /gyms

Running the base endpoint in PowerShell with a PUT method adds a new [`gym`](gym.md) object.

You can read a full tutorial on adding a new gym in Postman [`here`](../tutorials/add-a-new-gym.md).

## URL

```shell

{server_url}/gyms
```

## Request headers

This call uses `Content-Type: application/json` for the header.

## Request body

Take a look at the parameters for the request body in the following table.
If you leave any parameters out,
the system creates the entry without it.
The only obligatory parameter is the `lifterId`.
Without `lifterId`, the system returns an error.

If you don't give an ID value for the gym, the system assigns this value itself.
The parameter for this ID is `id`.

| Parameter | Example value | Obligatory |
| ------------- | ----------- | ----------- |
| `lifterId` | 1 | Yes |
|  `name` | `Deadlift Dungeon` | No |
| `description` | `Strength-focused gym with calibrated plates and a deadlift-only platform.` | No |
|  `location` | `Baltimore, MD` | No |
|  `rating` | 5 | No |

## Example

```js

curl -X POST "http://localhost:3000/gyms" \
  -H "Content-Type: application/json" \
  -d '{
    "lifterId": 1,
    "name": "Deadlift Dungeon",
    "description": "Strength-focused gym with calibrated plates and a deadlift-only platform.",
    "location": "Baltimore, MD",
    "rating": 5
    }'
```

Here, `-H` marks the header and `-d` marks the request body.
Backslashes make the code more easily readable.

## Return body

```js
{
    "lifterId": 1,
    "name": "Deadlift Dungeon",
    "description": "Strength-focused gym with calibrated plates and a deadlift-only platform.",
    "location": "Baltimore, MD",
    "rating": 5,
    "id": 5
} 
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data added successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
