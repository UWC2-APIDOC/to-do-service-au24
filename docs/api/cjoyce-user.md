# `user` resource

Contains details about the users of the service.

## Base endpoint:

```shell

{server_url}/users
```

## Resource properties

Sample `user` resource

```js

{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name |
| `first_name` | string | The user's first name |
| `email` | string | The user's email address |
| `id` | number | The user's unique record ID |

## Tutorials

* [Enroll a new user](https://github.com/cnjoyce1225/to-do-service-au24/blob/b4f835b01f271d14f87f50e1213c8dfc8dc59eb9/docs/tutorials/tutorial_cjoyce.md)
