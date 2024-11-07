---
layout: page
---

# Get task by user ID

Returns an array of  [`task`](task.md) objects that relate to the user specified by the `user_id` parameter.

## URL

```shell

{server_url}/tasks?user_id={user_id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `user_id` | number | The record ID of the user property found on all returned tasks |

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
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user_id record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
