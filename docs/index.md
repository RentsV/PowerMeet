---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
# tags used by AI files
description: Describes PowerMeet for a new user
tags: 
    - introduction
categories: 
    - tutorial
ai_relevance: high
importance: 9
prerequisites: []
related_pages: 
    - /before-you-start-a-tutorial
    - /quickstart 
    - /apy/gym
    - /api/lifter
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-11-21"
# vale  on
# markdownlint-enable
---

# PowerMeet API

![PowerMeet image](/powermeet.png)

This is a mock API to simulate the REST interface of an
imaginary service.

PowerMeet helps powerlifters find other lifters and suitable gyms.
This API has two resources: lifters and gyms.
You can query the system to see information about a specific lifter or a gym.
You can also see the list of all lifters or all gyms, along with available information.
This way, lifters know right away if a gym has the equipment they need.

Heck, no one really cares about security here, so you can even edit or delete
all the entries without verifying your identity.
At least in your own cloned repo, you're the king, queen, and the court.

## Quickstart

[Add your first lifter and their gym](quickstart.md).
It's like a piece of cake during your bulking phase.

## Tutorials

Learn how to do common tasks.

First, complete this tutorial to set up your development system for these tutorials.
You only have to do this one time per development system.

* [Before you start a tutorial](before-you-start-a-tutorial.md)

After your system is ready, these tutorials show you how to perform the main tasks.

* [See all lifters](tutorials/get-all-lifters.md)
* [Add a new lifter](tutorials/add-a-new-lifter.md)
* [See all gyms](tutorials/get-all-gyms.md)
* [Add a new gym](tutorials/add-a-new-gym.md)

To see a list of all tutorials, visit the [tutorials page](tutorials.md).
This includes tutorials for editing and deleting both lifter and gym entries.

According to the interviews, most lifters don't feel comfortable using PowerShell.
To meet their needs, these tutorials focus on using the API in Postman.
If you want to use a shell,
you'll find your answers in API reference docs.

## API reference docs

API reference docs include detailed descriptions of the service's resources.

These docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.

* [The lifter resource](api/lifter.md)
* [The gym resource](api/gym.md)
