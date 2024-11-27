---
layout: page
---

# Revise a task due date

Updates the `due_date` of an existing task. This can be useful when the task's deadline needs to be adjusted.

## URL

```shell
{base_url}/tasks/{id}
```

## Method
`PATCH`

## Params

| Parameter name | Type   | Description |
| -------------- | ------ | ----------- |
| `id`           | number | The record ID of the task to update |

## Request headers

| Header name    | Type   | Description                           |
| -------------- | ------ | ------------------------------------- |
| `Content-Type` | string | Must be set to `application/json`     |

## Request body

| Property name | Type   | Description |
| -------------- | ------ | ----------- |
| `due_date`     | string | The date in ISO 8601 format         |

## Example request

In this example, we are adjusting the due date for task 5 in the resource

```bash
curl -X PATCH "{base_url}/tasks/5" \
     -H "Content-Type: application/json" \
     -d '{"due_date": "2024-12-01T17:00"}'
```

## Example response

```json
{
  "user_id": 5,
  "title": "Buy groceries",
  "description": "Milk, bread, butter, eggs",
  "due_date": "2024-12-01T17:00",
  "warning": "-15",
  "id": 5
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified task record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |


