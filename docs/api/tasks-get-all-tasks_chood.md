---
layout: page
---

# Get all tasks

This method returns an array of [`task`](task.md) objects that contain all tasks registered with the service.

## URL

```shell

{base_url}/tasks
```

## Params

None

## Request headers

None

## Request body

None

## Return body

```js
[
    {
        "user_id": 1,
        "title": "Doctor's appt",
        "description": "annual checkup",
        "due_date": "2024-02-20T17:00",
        "warning": "-30",
        "id": 1
    },
    {
        "user_id": 1,
        "title": "Get lunch w/John",
        "description": "Get lunch at work with John",
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
        "title": "Vet appt",
        "description": "Annual vaccinations for cat",
        "due_date": "2024-05-11T14:00",
        "warning": "-20",
        "id": 4
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## READ
* [DELETE a task](../tutorials/delete-a-task_chood.md)
* [Task Resource](task.md)
