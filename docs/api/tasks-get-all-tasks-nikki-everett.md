---
layout: page
---

# Get all tasks

Returns an array of [`task`](task.md) objects that contains all tasks that users have created with the service.

## URL

```shell

{server_url}/tasks
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

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
