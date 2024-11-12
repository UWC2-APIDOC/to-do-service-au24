---
layout: page
---

# `task` resource - Get Task by User ID

Base endpoint:

```shell
{base_url}/tasks?user_id={user_id}
```

Retrieves all tasks associated with a specific user based on the provided `user_id`.

To use this endpoint, the user must be added to the service first. Learn more about the [user resource](user.md).

## Request

### Parameters

| Parameter | Type | Description |
| --------- | ---- | ----------- |
| `user_id` | number | The ID of the user whose tasks should be retrieved |

Example request:

```shell
curl http://localhost:3000/tasks?user_id=1
```

## Response

A successful response returns a list of tasks associated with the specified `user_id`. If no tasks are found, an empty array is returned.

### Sample Response

```json
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
  }
]
```

### Error Response

If the `user_id` is not found or invalid, an error message will be returned.

#### Sample Error Response

```json
[]
```

## Resource Properties

| Property name | Type | Description |
| ------------- | ---- | ----------- |
| `user_id`     | number | The ID of the user resource to which this task is assigned. Must be a valid, positive integer. |
| `title`       | string | The title or short description of the task |
| `description` | string | The long description of the task |
| `due_date`    | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning`     | number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`. |
| `id`          | number | The task's unique record ID |
