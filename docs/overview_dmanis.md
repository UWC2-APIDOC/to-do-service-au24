---
layout: page 
---

# To-Do service  

Track your tasks online and get reminders wherever you go. Use a REST interface to create users and add tasks.  

[Installation](#installation)  
[Tutorials](#tutorials)  
[API reference](#api-reference)  

## Installation  

[Install To-Do service](before-you-start-a-tutorial.md)

## Tutorials  

Learn the system by creating a new user and a new task.

### [Enroll a new user](tutorials/enroll-a-new-user.md)

Add a new user to your system so that you can assign them tasks.

Example request:  

```json
{
    "last_name": "Jones",
    "first_name": "Jenny",
    "email": "jen.jones@example.com"
}
```

Example response:  

```json
{
    "last_name": "Jones",
    "first_name": "Jenny",
    "email": "jen.jones@example.com",
    "id": 5
}
```

Learn more in the [Enroll a new user](tutorials/enroll-a-new-user.md) tutorial.

### [Add a new task](tutorials/add-a-new-task.md)  

Create a task and assign it to someone.

Example request:  

```json
{
    "user_id": 3,
    "title": "Get new tires",
    "description": "Get new tires for Hoppity",
    "due_date": "2024-03-11T14:00",
    "warning": "-60"
}
```

Example response:  

```json
{
    "user_id": 3,
    "title": "Get new tires",
    "description": "Get new tires for Hoppity",
    "due_date": "2024-03-11T14:00",
    "warning": "-60",
    "id": 5
}
```

Learn more in the [Add a new task](tutorials/add-a-new-task.md) tutorial.

## API reference  

Detailed descriptions of the service's resources.

Note that the API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.

* [user resource](api/user.md)
* [task resource](api/task.md)

## Links  

* [Installation](before-you-start-a-tutorial.md)
* [Tutorials](overview_dmanis.md#tutorials)
* [API reference](overview_dmanis.md#api-reference)
