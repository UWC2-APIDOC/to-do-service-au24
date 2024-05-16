---
layout: page
---
# `task` resource

Base endpoint:

```shell

{server_url}/tasks
```

Contains information about tasks stored for the users of the service.

To have a task in the service, the user must be added to
the service first. Learn more about the [user resource](user.md). 

## Resource properties

Sample `task` resource

```js

{
    "user_id": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | number | The ID of the user resource to which this task is assigned |
| `title` | string | The title or short description of the task |
| `description` | string | The long description of the task|
| `due_date` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`.|
| `id` | number | The task's unique record ID |

## READ

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID _(coming soon)_](#resource-properties)
* [Get task by user ID _(coming soon)_](#resource-properties)
