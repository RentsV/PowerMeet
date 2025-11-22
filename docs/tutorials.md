---
# markdownlint-disable
# vale  off
layout: default
nav_order: 6
has_children: true
has_toc: false
# tags used by AI files
description: Lists the tutorials available in the documentation
tags: 
    - introduction
categories:
    - tutorial
ai_relevance: high
importance: 8
prerequisites: []
related_pages: 
    - /tutorials/add-a-new-gym
    - /tutorials/add-a-new-lifter
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-11-07"
# vale  on
# markdownlint-enable
---

# Tutorials

![Tutorials image](/tutorials.png)

These tutorials are available to help you start using the **PowerMeet API**.
They cover five basic API operations:

* GET - retrieves all information about the resource.
* POST - creates a new entry.
* PATCH - updates an existing entry.
* PUT - replaces an existing entry with a new one.
* DELETE - deletes an entry.

First, there is a list of all `lifter` operations,
as a lifter resource must exist to create a new gym entry.
Then, there is a list of all `gym` operations.

## Before you start

Be sure to review [Before you start a tutorial](before-you-start-a-tutorial.md)
before you start trying out these operations.

## The `lifter` resource

* [Get a list of all lifters](tutorials/get-all-lifters.md)
* [Get a lifter by ID](tutorials/get-a-lifter-by-id.md)
* [Add a new lifter](tutorials/add-a-new-lifter.md)
* [Edit a lifter entry](tutorials/edit-a-lifter.md)
* [Delete a lifter](tutorials/delete-lifter.md)

## The `gym` resource

* [Get a list of all gyms](tutorials/get-all-gyms.md)
* [Get a gym by ID](tutorials/get-a-gym-by-id.md)
* [Add a new gym](tutorials/add-a-new-gym.md)
* [Edit a gym](tutorials/edit-a-gym.md)
* [Delete a gym](tutorials/delete-gym.md)
