---
layout: page
---

# Get all tasks

**GET** `/tasks`

Get all [`tasks`](task.md) that have been added to the service.

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

## Response body

Returns an array of [`task`](task.md) objects.

### Example response body

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
  ...
]
```

## Response status

| Status value | Response status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully. |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
