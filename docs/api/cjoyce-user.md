# `user` resource

Contains details about the users of the service. A user must be added to the service before they can add a [task](https://github.com/cnjoyce1225/to-do-service-au24/blob/65725a13e9c10c6daaccdf216c7dbd0d45e02c8d/docs/api/task.md).

## Endpoints:
<details><summary>Base endpoint</summary>

```shell

{server_url}/users
```

</details>

<details><summary>Example: lookup by user ID</summary>

```shell

{server_url}/users/3
```

</details>


## Resource properties

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name |
| `first_name` | string | The user's first name |
| `email` | string | The user's email address |
| `id` | number | The user's unique record ID |

### Sample `user` resource

```js

{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
}
```

## Tutorials

* [Enroll a new user](https://github.com/cnjoyce1225/to-do-service-au24/blob/b4f835b01f271d14f87f50e1213c8dfc8dc59eb9/docs/tutorials/tutorial_cjoyce.md)
