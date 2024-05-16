---
layout: page
---

# Get user by ID

Returns an array of  [`user`](user) objects that contains only the user specified by the `id` parameter, if it exists.

## URL

```shell

{server_url}/users/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the user to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
        "last_name": "Smith",
        "first_name": "Ferdinand",
        "email": "f.smith@example.com",
        "id": 1
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
