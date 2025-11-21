---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 2
# tags used by AI files
description: Get a list of a `lifter` resource by ID
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
    - GET /lifters/{id}
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Tutorial: Get a lifter by ID

In this tutorial, you learn to use the GET call to retrieve information about a specific lifter.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Get a list of all lifters

Retrieving this information requires you to use the `GET` method.

To retrieve information about a chosen lifter:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/lifters/{id}` where {id} is an ID number.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        This call doesn't need a request body.

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body. If your URL ended with 1, the response should look something like this.

    ```js
    {
        "lastName": "Johnson",
        "firstName": "Tara",
        "email": "tara.johnson@example.com",
        "id": 1
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
