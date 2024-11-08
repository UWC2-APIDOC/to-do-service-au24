---
layout: page
---

# Get tasks

## Base endpoint

```shell
{server_url}/tasks
```

## Description

Returns an array of [`task`](task.md) objects. The array contains all tasks that have been created with your To-Do Service.

`Get tasks` does not have a request body, parameters, or headers.

## Return body example

The following example of **Get tasks** returns an array containing four tasks:

```js
[
  {
    "user_id": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "id": 1
  },
  {
    "user_id": 1,
    "title": "Piano recital",
    "description": "Daughter's first concert appearance",
    "due_date": "2024-04-02T15:00",
    "warning": "-30",
    "id": 2
  },
  {
    "user_id": 2,
    "title": "Oil change",
    "description": "5K auto service",
    "due_date": "2024-03-10T09:00",
    "warning": "-60",
    "id": 3
  },
  {
    "user_id": 3,
    "title": "Get shots for dog",
    "description": "Annual vaccinations for poochy",
    "due_date": "2024-05-11T14:00",
    "warning": "-20",
    "id": 4
  }
]

```

## Return properties

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | integer | The `user_id` that the task is assigned to. |
| `title` | string | The task name. |
| `description` | string | The task description. |
| `due_date` | string | The task due date, formatted in ISO 8601. |
| `warning` | integer | The number of days before the task `due_date` where the `user_id` receives a warning. |
| `id` | integer | The task id. |


## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. |