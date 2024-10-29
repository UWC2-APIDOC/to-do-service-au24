---
layout: page
---

# Tutorial: Add a user

This tutorial will teach you how to add a new user to the To-Do system.

Allow 30 minutes to complete this lesson.

## Prerequisites

* The To-Do service is up and running. Follow [the setup procedure](../before-you-start-a-tutorial.md) to install and run the To-Do service on your local system.
* You are comfortable working with [REST interfaces](https://restfulapi.net).
* A REST client such as [cURL](https://curl.se), [Postman](https://www.postman.com), or [Insomnia](https://insomnia.rest). This tutorial assumes you are using cURL but use whatever REST client you like.

## Steps

Note: This tutorial assumes that the To-Do service is running at http://localhost:3000. Remember to point to your own host when you adapt the code samples to your own environment.

You create new users to the system with the POST method of the 'Create User' API. 

1. Submit a Create User request with the following user details: 

    * first name
    * last name
    * email address

    Example request:

    ```shell
    curl -XPOST -H "Content-type: application/json" -d '{
        "first_name": "Mercedes",
        "last_name": "Hernandez",
        "email": "mercedes@example.com"
    }' 'http://localhost:3000/users'
    ```

    The service responds with the user details that you submitted and a unique ID that the system generates automatically.

    Example response:

    ```json
    {
    "first_name": "Mercedes",
    "last_name": "Hernandez",
    "email": "mercedes@example.com",
    "id": 5
    }
    ```

1. Verify that the response data matches the user details that you submitted.

    If the data matches, congratulations! your new user is in the system and ready to receive tasks. Note the unique ID; you will need to know it if you want to fetch your user's details later. 


## Fetch your user's details 

You can fetch your user's details any time with the GET method of the 'users' resource with the unique ID set by the server. 

Example 'get user details' request:

```shell
curl http://localhost:3000/users/5
```

Response:
```json
{
  "first_name": "Mercedes",
  "last_name": "Hernandez",
  "email": "mercedes@example.com",
  "id": 5
}
```

## Fetch details for all users in the system 

You can fetch the details of every user in the system with the GET method of the 'users' resource. 

Example 'get users' request: 

```shell
curl http://localhost:3000/users
```

Response:

```json
[
  {
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
  },
  {
    "last_name": "Jones",
    "first_name": "Jill",
    "email": "j.jones@example.com",
    "id": 2
  },
  {
    "last_name": "Martinez",
    "first_name": "Marty",
    "email": "m.martinez@example.com",
    "id": 3
  },
  {
    "last_name": "Bailey",
    "first_name": "Bill",
    "email": "b.bailey@example.com",
    "id": 4
  },
  {
    "first_name": "Mercedes",
    "last_name": "Hernandez",
    "email": "mercedes@example.com",
    "id": 5
  }
]
```

## Links

* [Tutorial: Add a new task](add-a-new-task.md)
