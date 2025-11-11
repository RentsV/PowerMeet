---
# markdownlint-disable
# vale  off
layout: default
nav_order: 2
parent: Tutorials
# tags used by AI files
description: Add a `gym` resource to the service
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/lifter
    - /api/gym
related_pages: []
examples: []
api_endpoints:
    - POST /gyms
version: "v1.0"
last_updated: "2025-10-07"
# vale  on
# markdownlint-enable
---

# Tutorial: Add a new gym

In this tutorial, you learn to add a new gym.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Add a new gym

Adding a new gym to the service requires that you use the `POST` method.
This allows you to store the details of the new [`gym`](../api/gym.md) resource in the service.

To add a new gym:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{base_url}/gyms`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```js
        {
            "lifterId": 3,
            "name": "My Favourite Gym",
            "description": "Lacks all basic necessities, avoid.",
            "location": "Newark, NJ",
            "rating": 1
        }
        ```

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this.
6. Note that the names should be the same as you used in your **Request body**.
7. The response should include the new user's ID.

    ```js
    {
        "lifterId": 3,
        "name": "My Favourite Gym",
        "description": "Lacks all basic necessities, avoid.",
        "location": "Newark, NJ",
        "rating": 1
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
