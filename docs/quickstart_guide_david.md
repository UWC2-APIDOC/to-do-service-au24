[Back to Landing Page](overview_david.md)

# Quickstart Guide

*Welcome to the To-Do Service API! This guide will help you get started quickly by showing you how to enroll a new user and add a task using our API with Postman.*

## Overview

In this quickstart, you will:

- Enroll a new user into the To-Do Service.
- Add a new task for that user.
- Retrieve the list of tasks to confirm your additions.

**Estimated time to complete:** 10 minutes

## Prerequisites

Read the [Before you start a tutorial](before-you-start-a-tutorial.md) for prerequisites.

## Step 1: Start the To-Do Service API

Start the API server using `json-server` in the `api` directory:

```shell
json-server -w to-do-db-source.json
```
This will start the server at `http://localhost:3000`. Set this as an environment variable for base_url in Postman, otherwise you can use `http://localhost:3000` in place of `{{base_url}}`.

## Step 2: Enroll a New User

1. Open Postman and create a new **POST** request to `{{base_url}}/users`.

2. In the **Headers** tab, verify:
- Key: `Content-Type`
- Value: `application/json`

3. In the **Body** tab, select **raw** and choose **JSON**.

4. Enter the following JSON data:

```json
{
  "first_name": "Alice",
  "last_name": "Anderson",
  "email": "alice.anderson@example.com"
}
```

5. Click **Send**.

### Response

You should receive a response with the new user data, including an `id`:

```json
{
  "first_name": "Alice",
  "last_name": "Anderson",
  "email": "alice.anderson@example.com",
  "id": 5
}
```

Note: Remember the `id` of the new user (e.g., `5`) for the next step.

## Step 3: Add a New Task for the User

1. Create a new **POST** request to `{{base_url}}/tasks`.

2. In the **Headers** tab, verify:
- Key: `Content-Type`
- Value: `application/json` header`.

3. In the **Body** tab, select **raw** and choose **JSON**.

4. Enter the following JSON data:

```json
{
  "user_id": 5,
  "title": "Finish API Documentation",
  "description": "Complete the first-use topic and tutorial",
  "due_date": "2024-11-01T17:00",
  "warning": -30
}
```

5. Click **Send**.

### Response

You should see the new task with an assigned `id`:

```json
{
    "user_id": 5,
    "title": "Finish API Documentation",
    "description": "Complete the first-use topic and tutorial",
    "due_date": "2024-11-01T17:00",
    "warning": -30,
    "id": 5
}
```

## Step 4: Retrieve the User's Tasks

1. Create a new **GET** request to `{{base_url}}/tasks?user_id=5` where `user_id` is the `id` for the user created in Step 2 above. In our example, the `user_id` is `5`.

2. Click **Send**.

### Response

You should receive an array of tasks for the user:

```json
[
    {
        "user_id": 5,
        "title": "Finish API Documentation",
        "description": "Complete the first-use topic and tutorial",
        "due_date": "2024-11-01T17:00",
        "warning": -30,
        "id": 5
    }
]
```

# Next Steps

Congratulations! You've successfully enrolled a new user and added a task using the To-Do Service API with Postman.

- **Explore more:**
  - Add additional users and tasks.
  - Try updating or deleting tasks using the API.
- Check out the [API Reference: Task by User ID](api/api_reference_task_by_user_id_david.md) on how to retrieve all tasks associated with a specific user based on the provided `user_id`.