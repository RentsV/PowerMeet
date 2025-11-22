---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 4
# tags used by AI files
description: Edit a `lifter` resource
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
    - POST /lifters/{id}
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Edit a lifter

In this tutorial, you learn the operations to edit a `lifter` entry.
You have two options for editing an entry.
You can use the PATCH call to only edit certain fields of an existing entry.
The other option is to use the PUT call that replaces the whole entry.
The first is easier, as the request body only consists of relevant fields.
For the PUT call, you have to enter all the fields
or the system overwrites the fields you left out and marks them empty.

Expect this tutorial to take about 25 minutes to complete.

## Before you start

Make sure you've completed the instructions in [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Edit a lifter with PATCH

This method replaces some details of a [`lifter`](../api/lifter.md) resource in the service.

To edit a `lifter` entry:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, find the entry you want to change. It might look like this:

    ```js
    {
        "lastName": "Johnson",
        "firstName": "Tara",
        "email": "tara.johnson@example.com",
        "id": 1
    }
    ```

4. Create a new request with these values:

    * **METHOD**: PUT
    * **URL**: `{base_url}/lifters/{id}` where {id} is a numerical ID of your chosen lifter.

        > **Note:** Following the example, ID would be 1.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        Only write the values of properties you want to change.
        In this example, Tara married and is only updating her last name.

        ```js
        {
            "lastName": "Friedman"
        }
        ```

5. In the Postman app, choose **Send** to make the request.
Watch for the response body, which should look something like this.
Note that the information should be the same as you used in your **Request body**.

    ```js
    {
        "lastName": "Friedman",
        "firstName": "Tara",
        "email": "tara.johnson@example.com",
        "id": 1
    }
    ```

## Edit a lifter with PUT

This method replaces the details of a [`lifter`](../api/lifter.md) resource in the service.

To edit a `lifter` entry:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, find the entry you want to change. It might look like this:

    ```js
    {
        "lastName": "Johnson",
        "firstName": "Tara",
        "email": "tara.johnson@example.com",
        "id": 1
    }
    ```

4. Create a new request with these values:

    * **METHOD**: PUT
    * **URL**: `{base_url}/lifters/{id}` where {id} is a numerical ID of your chosen lifter.

        > **Note:** Following the example, ID would be 1.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        You can change the values of each property as you'd like, even the ID.
        In this example, Tara is on the run and has to take on a whole new identity.
        > **Warning:** The fields you don't mention are overwritten as empty.

        ```js
        {
            "lastName": "Friedman",
            "firstName": "Merilyn",
            "email": "merilyn.friedman@example.com",
            "id": 6
        }
        ```

5. In the Postman app, choose **Send** to make the request.
Watch for the response body, which should look something like this.
Note that the information should be the same as you used in your **Request body**.

    ```js
    {
        "lastName": "Friedman",
        "firstName": "Merilyn",
        "email": "merilyn.friedman@example.com",
        "id": 6
    }
    ```

## What's next?

After completing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

If you would like to learn how to do this in a shell,
read more about the [PATCH](../api/lifters-patch-lifter.md) and [PUT](../api/lifters-put-lifter.md)
operations for this endpoint.
