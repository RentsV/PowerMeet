---
# markdownlint-disable
# vale  off
layout: default
parent: Tutorials
nav_order: 7
# tags used by AI files
description: DELETE the `gym` resource with the specified ID from the service
tags:
    - api
categories:
    - api-reference
ai_relevance: high
importance: 7
prerequisites: 
    - /api/gym
related_pages: []
examples: []
api_endpoints: 
    - DELETE /gyms/{id}
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# Delete a gym by ID

In this tutorial, you learn to run a DELETE call.
This action deletes a [`gym`](../api/gym.md) object specified by the `id` parameter of the `gym` resource.

**Note:** If you run this call with no ID, you delete all gyms in the database!!!

## Before you start

Make sure you've completed the instructions in [Before you start a tutorial](../before-you-start-a-tutorial.md).

## Delete a gym

You must use the `DELETE` method to delete a gym.

To do so:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/powermeet/api
    json-server -w powermeetdb-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with these values:
    * **METHOD**: DELETE
    * **URL**: `{base_url}/lifters/{id}` where {id} is an ID number.
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        This call doesn't need a request body.

4. In the Postman app, choose **Send** to make the request.
5. This call also doesn't return anything, no matter if the call is successful or not.
To verify whether the deletion was successful, check the list of all gyms again.
Another option is to run a GET call with this ID to make sure that it doesn't exist anymore.
If in doubt, check out the relevant tutorials for [checking the list of all gyms](/get-all-gyms.md)
or [retrieving information about a specific gym](/get-a-gym-by-id.md).

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
