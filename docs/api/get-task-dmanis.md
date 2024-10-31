---
layout: page
---

# Get User
The Get User service fetches the details for a given user in the system.

## URL
{host}/tasks/{taskID}

## HTTP method
GET

## Request headers
None

## Request parameters

| Name          | Type          | Mandatory? | Constraints | Description |
| ------------- | ------------- | ---        | ---         | ---         |
| taskID        | int           | true       | Must be a positive integer. | The system-generated unique identifier for the task. |

## Request content
None

## Response content

| Name          | Type          | Mandatory? | Constraints | Description |
| ------------- | ------------- | ---        | ---         | ---         |
| user_id       | int           | true       | -           | Unique ID of the user assigned to the task. |
| title         | string        | true       | -           | -           |
| description   | string        | true       | -           | -           |
| due_date      | date          | true       | datetime    | The date and time that the task is due. |
| warning       | float          | true       | -           | The system will send an alert to the user {warning} days before the task is due. |
| id            | int           | true       | -           | System-generated unique identifier of the task. |

## HTTP response codes

| Code          | Description   | Notes |
| ------------- | ------------- | ---   |
| 200           | OK            | -     |

## Example request and response

Request:
```bash
curl http://localhost:3000/tasks/1
```

Response:
```json
{
  "user_id": 1,
  "title": "Grocery shopping",
  "description": "eggs, bacon, gummy bears",
  "due_date": "2024-02-20T17:00",
  "warning": "-10",
  "id": 1
}
```
