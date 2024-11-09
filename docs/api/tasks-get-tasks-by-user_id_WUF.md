---
layout: page
---

# Get tasks by User ID

Returns an array of [`task`](task.md) objects that contain a specified `user_id` parameter.

## URL

```shell

{base_url}/tasks?user_id=1
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `user_id` | number | The ID of the user resource to which a task is assigned |

## Request headers

None

## Request body

None

## Return body

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
        "due_date": "2024-03-10T09:00",
        "warning": "-30",
        "id": 2
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
