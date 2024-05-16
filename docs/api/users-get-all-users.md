---
layout: page
---
# Get all users

Returns an array of [`user`](user) objects that contains all users that have registered with the service.

## URL

```shell

{server_url}/users
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
        "last_name": "Smith",
        "first_name": "Ferdinand",
        "email": "f.smith@example.com",
        "id": 1
    },
    {
        "last_name": "Jones",
        "first_name": "Jillio",
        "email": "jlo.jones@example.com",
        "id": 2
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
