---
# markdownlint-disable
# vale  off
layout: default
nav_order: 5
has_children: true
has_toc: false
# tags used by AI files
description: "Information about the `gym` resource"
tags: 
    - api
categories: 
    - api-reference
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/add-a-new-gym
examples: []
api_endpoints:
    - /gyms
    - /gyms{id}
version: "v1.0"
last_updated: "2025-11-22"
# vale  on
# markdownlint-enable
---

# The `gym` resource

![Location image](../locations.png)

Base endpoint:

```shell

{server_url}/gyms
```

Contains information about all the gyms stored by the service.

To have a gym in the service, the lifter must already exist in the system.
Learn more about the [lifter resource](lifter.md).

## Resource properties

Sample `gym` resource

```js

{
    "lifterId": 2,
    "name": "Foundry Strength and Conditioning",
    "description": "Strongman and powerlifting gym with open platform space and deadlift bars.",
    "location": "Jersey City, NJ",
    "rating": 4,
    "id": 2
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `lifterId` | number | ID of the lifter resource associated with this gym |
| `name` | string | Name of the gym |
| `description` | string | Description of the gym|
| `location` | string | Location of the gym |
| `rating` | number | Rating of the gym from 1 to 5 |
| `id` | number | The gym's unique record ID |

## Available operations

* [GET /gyms](gyms-get-all-gyms.md)
* [GET /gyms{id}](gyms-get-gym-by-id.md)
* [POST /gyms](gyms-post-gym.md)
* [PUT /gyms{id}](gyms-put-gym.md)
* [PATCH /gyms{id}](gyms-patch-gym.md)
* [DELETE /gyms{id}](gyms-delete-gym-by-id.md)
