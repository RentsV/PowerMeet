---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 4
# tags used by AI files
description: Get a list of all `gym` resources
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
    - GET /gymss
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Get all gyms

In this tutorial, you learn to use the GET call to retrieve a list of all gyms.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Get a list of all gyms

Retrieving a list of all gyms requires you to use the `GET` method.

To get a list of all gyms:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: GET
    * **URL**: `{base_url}/gyms`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        This call doesn't need a request body.

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this.

    ```js
    [
        {
            "lifterId": 1,
            "name": "Iron Temple Barbell Club",
            "description": "Powerlifting: combo racks, chalk-friendly policy, calibrated plates.",
            "location": "Newark, NJ",
            "rating": 5,
            "id": 1
        },
        {
            "lifterId": 2,
            "name": "Foundry Strength and Conditioning",
            "description": "Strongman and powerlifting gym with open platform space and deadlift bars.",
            "location": "Jersey City, NJ",
            "rating": 4,
            "id": 2
        },
        ...
    ]
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
