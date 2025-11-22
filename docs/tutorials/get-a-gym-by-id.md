---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 7
# tags used by AI files
description: Get an instance of a `gym` resource by ID
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
    - GET /gyms/{id}
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Get a gym by ID

In this tutorial, you learn to use the GET call to retrieve information about a specific gym.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the instructions in [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Retrieve a gym by ID

Retrieving this information requires you to use the `GET` method.

To retrieve information about a chosen gym:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/gyms/{id}` where {id} is a numerical ID of your chosen gym.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        This call doesn't need a request body.

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body. If your URL ended with 1, the response should look something like this.

    ```js
    {
        "lifterId": 1,
        "name": "Iron Temple Barbell Club",
        "description": "Powerlifting: combo racks, chalk-friendly policy, calibrated plates.",
        "location": "Newark, NJ",
        "rating": 5,
        "id": 1
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

If you would like to learn how to do this in a shell,
read more about the [GET](../api/gyms-get-gym-by-id.md) operation for this endpoint.
