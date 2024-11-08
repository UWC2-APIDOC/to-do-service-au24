---
layout: page
---

# Tutorial: Add a user

With the To-Do service you can assign tasks to users, track the status of tasks, and notify users when their tasks are due. To enjoy these features you must first have a user to assign tasks to. This tutorial will teach you how to add a new user to the To-Do system and fetch your new user's details.

Allow 30 minutes to complete this lesson.

## Prerequisites

* The To-Do service is up and running. Follow [the setup procedure](../before-you-start-a-tutorial.md) to install and run the To-Do service on your local system.
* You are comfortable working with [REST interfaces](https://restfulapi.net).
* A REST client such as [cURL](https://curl.se), [Postman](https://www.postman.com), or [Insomnia](https://insomnia.rest). This tutorial assumes you are using cURL but use whatever REST client you like.

## Overview

The following procedures will teach you how to [Create a new user](#create-a-new-user) and to [Fetch your new user's details](#fetch-your-new-users-details). When you've completed the procedures you will have a new user ready to receive tasks and notifications.

### Create a new user

Note: This tutorial assumes that the To-Do service is running at http://localhost:3000. Remember to point to your own host when you adapt the code samples to your own environment.

You create new users to the system with the POST method of the 'Create User' API.

1. Submit a Create User request with the following user details:

    * first name
    * last name
    * email address

    Example request:

    ```shell
    curl -XPOST -H "Content-type: application/json" -d '{
        "first_name": "Mercedes",
        "last_name": "Hernandez",
        "email": "mercedes@example.com"
    }' 'http://localhost:3000/users'
    ```

    The service responds with the user details that you submitted and a unique ID that the system generates automatically.

    Example response:

    ```json
    {
    "first_name": "Mercedes",
    "last_name": "Hernandez",
    "email": "mercedes@example.com",
    "id": 5
    }
    ```

1. Verify that the response data matches the user details that you submitted.

    If the data matches, congratulations! Your new user is in the system and ready to receive tasks. Note the unique ID; you will need to know it if you want to fetch your user's details later.

### Fetch your new user's details

You can fetch your user's details any time with the GET method of the 'users' resource and the instance's unique ID.

Example 'get user details' request:

```shell
curl http://localhost:3000/users/5
```

Response:

```json
{
  "first_name": "Mercedes",
  "last_name": "Hernandez",
  "email": "mercedes@example.com",
  "id": 5
}
```

## What next?

Now that you have a user in the system, assign yourself some tasks as described in the [Create your first task](create_first_task_CT.md) tutorial.

## Links

* [Tutorial: Add a new task](add-a-new-task.md)
