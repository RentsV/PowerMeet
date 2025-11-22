---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 5
# tags used by AI files
description: DELETE the `lifter` resource with the specified ID from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites: 
    - /api/lifter
related_pages: []
examples: []
api_endpoints: 
    - DELETE /lifters/{id}
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Delete a lifter by ID

In this tutorial, you learn to run a DELETE call.
This action deletes a [`lifter`](../api/gym.md) object
specified by the `id` parameter of the `lifter` resource.

## Before you start

Make sure you've completed the instructions in [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Delete a lifter

You must use the `DELETE` method to delete a lifter.

To do so:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: DELETE
    * **URL**: `{base_url}/lifters/{id}` where {id} is an ID number of your chosen lifter.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        This call doesn't need a request body.

4. In the Postman app, choose **Send** to make the request.
5. This call doesn't return any text, no matter if the call is successful or not.
The only indicator of your success or failure is the little green `200 OK`
or red `404 Not Found` in Postman.
It should be above the empty response body, slightly to the right.
If you can't see it, or if you like double-checking,
you can run a GET call to make sure that this object doesn't exist anymore.
If in doubt, check out the relevant tutorials for [checking the list of all lifters](/get-all-lifters.md)
or [retrieving information about a specific lifter](/get-a-lifter-by-id.md).

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

If you would like to learn how to do this in a shell,
read more about the [DELETE](/api/lifters-delete-lifter-by-id.md) operation for this endpoint.
