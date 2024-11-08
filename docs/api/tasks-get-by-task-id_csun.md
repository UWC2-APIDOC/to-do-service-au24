---
layout: page
---

# Reference: Get tasks by id

Returns a [`task`](task.md) array that contains only the task resource specified by the `id` parameter, if it exists.

## URL

```shell
{base_url}/tasks/{id}
```

## Params

| Parameter name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The task's unique record ID |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
        "user_id": 1,
        "title": "Piano recital",
        "description": "Daughter's first concert appearance",
        "due_date": "2024-04-02T15:00",
        "warning": "-30",
        "id": 2
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related Topics

* [`Task`](task.md)
* [`Get all tasks`](tasks-get-all-tasks-nikki-everett.md)
* [`Get user by ID`](users-get-user-by-id.md)
