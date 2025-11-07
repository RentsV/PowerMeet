---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 2
# tags used by AI files
description: Add a `lifter` resource to the service
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites: 
    - /before-you-start-a-tutorial
    - /api/lifter
related_pages: []
examples: []
api_endpoints: 
    - POST /lifters
version: "v1.0"
last_updated: "2025-10-07"
# vale  on
# markdownlint-enable
---

# Tutorial: Add a new lifter

In this tutorial, you learn the operations to add a new lifter.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Add a new lifter

Adding a new lifter requires you to use the `POST` method.
This allows you to store the details of the new [`lifter`](../api/lifter.md) resource in the service.

To add a new lifter:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/lifters`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like.

        ```js
        {
            "lastName": "Jones",
            "firstName": "Jenny",
            "email": "jen.jones@example.com"
        }
        ```

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this.
6. Note that the names should be the same as you used in your **Request body**.
7. The response should include the new user's ID.

    ```js
    {
        "lastName": "Jones",
        "firstName": "Jenny",
        "email": "jen.jones@example.com",
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
