---
# markdownlint-disable
# vale  off
layout: default
nav_order: 3
has_children: false
has_toc: false
# tags used by AI files
description: Quickstart
tags: 
    - introduction
categories:
    - tutorial
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/add-a-new-lifter
    - /tutorials/add-a-new-gym
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Quickstart

![Tutorials image](/pmtutorials.png)

This quickstart walks you through creating yourself a new lifter
and then adding a gym to this lifter.
If you already have a lifter account, you can move straigth to [adding a gym](#add-a-gym) to an existing lifter.

## Before you start

Using this API requires your own fork of its repo, so
review [Before you start a tutorial](before-you-start-a-tutorial.md) before getting started.

## Add a lifter

To add a new lifter:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{base_url}/lifters`
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
Note that the names should be the same as you used in your **Request body**.
The response should include the new user's ID.

    ```js
    {
        "lastName": "Jones",
        "firstName": "Jenny",
        "email": "jen.jones@example.com",
        "id": 5
    }
    ```

## Add a gym

1. If you start from here, make sure your local service is running.
If it's not, start it by using this command.

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
        The `lifterId` is the ID you created in the previous step.

        ```js
        {
            "lifterId": 5,
            "name": "My Favourite Gym",
            "description": "Lacks all basic necessities, avoid.",
            "location": "Newark, NJ",
            "rating": 1
        }
        ```

4. In the Postman app, choose **Send** to make the request.
5. Watch for the response body, which should look something like this.
Note that the names should be the same as you used in your **Request body**.
The response should include the new gym's ID.

    ```js
    {
        "lifterId": 5,
        "name": "My Favourite Gym",
        "description": "Lacks all basic necessities, avoid.",
        "location": "Newark, NJ",
        "rating": 1
        "id": 5
    }
    ```

You are all set with both a lifter and a gym.
Check out the [tutorials page](tutorials.md) to learn about more operations.
