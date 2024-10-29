---
layout: page
---

# Get task by ID

GET {server_url}/task/{id}

Retrieves a task by the task id.

## Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The ID of the task to return |

## Request headers

None

## Request body

None

## Request example

```shell
    curl --location --request GET 'http://localhost:3000/tasks/4'
```

## Return example

```js
[
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

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
