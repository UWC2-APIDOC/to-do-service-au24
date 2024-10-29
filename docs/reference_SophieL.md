# [To-Do service](https://uwc2-apidoc.github.io/to-do-service-au24/)

## Get task by user ID
Get the list of [`tasks`](https://uwc2-apidoc.github.io/to-do-service-au24/api/task.html) associated with a specific [`user id`](https://uwc2-apidoc.github.io/to-do-service-au24/api/users-get-user-by-id.html), if it exists. 

## Request

**GET** /tasks?user_id={user_id}`

## Parameters
|Parameter name   |Type   |Description   |   
|---|---|---|
| `user_id`  |number   | The record ID of the user.  |   

## Response 
For details about the Response format, refer to the **Resource properties** section on the [`task`](https://uwc2-apidoc.github.io/to-do-service-au24/api/task.html#resource-properties) resource page.

## Response staus
|Status value   |Return status  |Description   |   
|---|---|---|
| 200  |OK (sucess)  | Request successful. The server has responded as required.  |  
|404|Not found|Requested resource could not be found.|
|ECONNREFUSED|N/A|Service is offline. Start the service and try again.|

## Sample request
`http://localhost:3000/tasks?user_id=1`

## Sample response
A list of tasks for the specified user.

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

**Note:** If the request is sucessful, but no task record is found (for example, the specified `user_id` does not exist), an empty array `[]` is returned.


