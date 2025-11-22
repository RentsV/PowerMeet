---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 9
# tags used by AI files
description: Edit a `gym` resource
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites: 
    - /before-you-start-a-tutorial
    - /api/gym
related_pages: []
examples: []
api_endpoints: 
    - PUT /gyms/{id}
    - PATCH /gyms/{id}
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Edit a gym

In this tutorial, you learn the operations to edit a `gym` entry.
You have two options for editing an entry.
You can use the PATCH call to only edit certain fields of an existing entry.
The other option is to use the PUT call that replaces the whole entry.
The first is easier, as the request body only consists of relevant fields.
For the PUT call, you have to enter all the fields
or the system overwrites the fields you left out and marks them empty.

Expect this tutorial to take about 25 minutes to complete.

## Before you start

Make sure you've completed the instructions in [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Edit a gym with PATCH

This method replaces some details of a [`gym`](../api/gym.md) resource in the service.

To edit a `gym` entry:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, find the entry you want to change. It might look like this:

      ```js
        {
            "lifterId": 4,
            "name": "Garage Grind Gym",
            "description": "Small private space focused on raw powerlifting training.",
            "location": "Harrison, NJ",
            "rating": 5,
            "id": 4
        }
        ```

4. Create a new request with these values:

    * **METHOD**: PUT
    * **URL**: `{base_url}/lifters/{id}`

        > :bulb: **Note:** Following the example, ID would be 4.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        Only write the values of properties you want to change.
        In this example, the gym has heating issues.

        ```js
        {
            "description": "Small, focused on raw powerlifting training. VERY COLD.",
            "rating": 3,
        }
        ```

5. In the Postman app, choose **Send** to make the request.
   Watch for the response body, which should look something like this.
   Note that the information should be the same as you used in your **Request body**.

    ```js
    {
        "lifterId": 4,
        "name": "Garage Grind Gym",
        "description": "Small, focused on raw powerlifting training. VERY COLD.",
        "location": "Harrison, NJ",
        "rating": 3,
        "id": 4
    }
    ```

## Edit a gym with PUT

This method replaces the details of a [`gym`](../api/gym.md) resource in the service.

To edit a `gym` entry:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, find the entry you want to change. It might look like this:

      ```js
        {
            "lifterId": 4,
            "name": "Garage Grind Gym",
            "description": "Small private space focused on raw powerlifting training.",
            "location": "Harrison, NJ",
            "rating": 5,
            "id": 4
        }
        ```

4. Create a new request with these values:

    * **METHOD**: PUT
    * **URL**: `{base_url}/gyms/{id}`

        > :bulb: **Note:** Following the example, ID would be 4.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like, even the ID.
        In this example, a bigger company bought it and changed things up.

        ```js
        {
            "lifterId": 4,
            "name": "MyFitness: Garage",
            "description": "Under renovation.",
            "location": "Harrison, NJ",
            "rating": 1,
            "id": 4
        }
        ```

        > :warning: **Warning:** The fields you don't mention are overwritten as empty.

5. In the Postman app, choose **Send** to make the request.
   Watch for the response body, which should look something like this.
   Note that the information should be the same as you used in your **Request body**.

    ```js
    {
        "lifterId": 4,
        "name": "MyFitness: Garage",
        "description": "Under renovation.",
        "location": "Harrison, NJ",
        "rating": 1,
        "id": 4
    }
    ```

## What's next?

After completing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

If you would like to learn how to do this in a shell,
read more about the [PATCH](/api/gyms-patch-gym.md) and [PUT](/api/gyms-put-gym.md)
operations for this endpoint.
