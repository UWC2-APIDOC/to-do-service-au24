---
layout: page
---

# TO Do Service Quick Start <!-- omit in toc -->

The **To Do Service API** is a cloud-based service that lets subscribers post to and review their task lists, and recieve reminders of tasks they'll need to complete. To start using this service, all you need is a user and a task!  
This quick start should take **15 minutes** to complete.

- [What you will learn](#what-you-will-learn)
- [Before you begin](#before-you-begin)
- [Users and Tasks](#users-and-tasks)
  - [Enroll a new user](#enroll-a-new-user)
  - [Add tasks](#add-tasks)
  - [Get the tasks for a user](#get-the-tasks-for-a-user)
- [Recap](#recap)
- [Learn more](#learn-more)

## What you will learn

- [How to add a user.](#enroll-a-new-user)
- [How to add tasks.](#add-tasks)
- [Get a list of tasks for a specific user.](#get-the-tasks-for-a-user)

## Before you begin

To sucessfully complete this quick start you will need to set up a test environment. Be sure to complete the [Before you start a tutorial](before-you-start-a-tutorial.md) before you start this quick start.

## Users and Tasks

The **To Do Service API** uses JSON files to create its database. In this tutorial, we will use cURL to `POST` and `GET` our data, but you can use any other REST client, such as Postman to send and receive data.

### Enroll a new user

Enrolling a new user in the service requires that you add `POST` the details of a new [`user`](api/user.md) resource to the service. The only information you need to add a user is

To enroll a new user:

1. If the To-Do service is not running, start it by using this command in your command-line tool.

    ```shell
    cd <your-github-workspace>/to-do-service/api 
    sh start-server.sh
    ```

2. Open another command-line window.
3. To create a new user resource, in the new command-line window, enter this curl command:

    ```shell
    curl -X POST http://localhost:3000/users \
    > -H "Content-Type: application/json" \
    > -d '{"last_name": "Fish", "first_name": "Wendy", "email": "wfish@example.com"}'
    ```

4. The curl command should display a response body like this with the user name you supplied. The response should also include a new user `id`.

    ```js
    {
        "last_name": "Fish",
        "first_name": "Wendy",
        "email": "wfish@example.com",
        "id": 7
    }
    ```

### Add tasks

Now we are going to add some tasks for our new user. Note that to do this we use a `POST` command that's similar to what we just used to create the `user` record. The difference is that now we need to supply the following task data.
The differences are that we are creating a `task` resource and providing the task data described here.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | number | The ID of the user resource to which this task is assigned |
| `title` | string | The title or short description of the task |
| `description` | string | The long description of the task|
| `due_date` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`.|



1. We'll use the `POST` command in our command-line tool to create a task for our new user to **get plane tickets from NYC to Portugal** before midnight on **11/01/24**. We will also send a reminder **24 hours** before the deadline.


    ```shell
        curl -X POST http://localhost:3000/tasks \
        > -H "Content-Type: application/json" \
        > -d '{"user_id": 7, "title": "Get plane tickets", "description": "Find a flight from NYC to Lisbon, Porto, or Sao Miguel", "due_date": "2024-11-01T23:59", "warning": "-1440"}'
    ```
2. The curl command should return something like this with a new task `id`.

    ```shell
    {
    "user_id": 7,
    "title": "Get plane tickets",
    "description": "Find a flight from NYC to Lisbon, Porto, or Sao Miguel",
    "due_date": "2024-11-01T23:59",
    "warning": "-1440",
    "id": 8
    }
    ```
1. Create some more tasks for your new user.

### Get the tasks for a user
Now we'll use the To-Do service to get all the tasks we created for our new user. This demonstrates a new way to get tasks from the To-Do service.
1. For this step, you need the `id` of the user you [enrolled earlier](#enroll-a-new-user).
1. Add the value of the new user's `id` as the value of the `user_id` parameter. In this example, the value of the  `user_id` is `7`.
   ```shell
    curl http://localhost:3000/tasks?user_id=7
    ```
1. The curl command should return all the [tasks you created](#add-tasks) earlier. The command should return something like this:

    ```shell
    {
        "user_id": 7,
        "title": "Call Liza",
        "description": "Portugal Itinerary",
        "due_date": "2024-11-04T09:00",
        "warning": "-15",
        "id": 5
    },
    {
        "user_id": 7,
        "title": "Dr. Ross",
        "description": "Annual Physical",
        "due_date": "2025-09-27T09:00",
        "warning": "-15",
        "id": 6
    },
    {
        "user_id": 7,
        "title": "Haircut",
        "description": "Signor Purelli Salon",
        "due_date": "2024-10-21T15:00",
        "warning": "-30",
        "id": 7
    },
    {
        "user_id": 7,
        "title": "Get plane tickets",
        "description": "Find a flight from NYC to Lisbon, Porto, or Sao Miguel",
        "due_date": "2024-11-01T23:00",
        "warning": "-1440",
        "id": 8
    }
    ```
## Recap
**Congratulations!!** You've successfully created a new user and saved some tasks. You also queried the To-Do service and received specific information about the user and their tasks. 
You can do so much more with the **To Do Service API**. To learn more about what is possible, we invite you to take a look at some of our other tutorials.

## Learn more

- [Delete a user](tutorials/enroll-a-new-user.md)

- [Update a task](tutorials/add-a-new-task.md)
