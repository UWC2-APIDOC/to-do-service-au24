---
layout: page
---

# Add a user

The To-do API lets you add users including their email address so that they can get reminders about upcoming tasks
This quickstart explains how to enroll your first user with the To-do API.

You need about 15 minutes to complete this quickstart.

## Step 1: Set up your environment

Review the  [Before you start a tutorial](../before-you-start-a-tutorial.md) to get your environment set up for the quickstart.

## Step 2: Add your first user

To add a new user run the following command.

```
curl --location 'http://localhost:3000/users' \
--header 'Content-Type: application/json' \
--data-raw '{
   "last_name": "Smith",
   "first_name": "Apple",
   "email": "apple.smith@example.com"
}'
```

## Step 3: Verify the response

The response is returned.  Make note of the user's id; it may be different in your response.

```
{
 "last_name": "Smith",
 "first_name": "Apple",
 "email": "apple.smith@example.com",
 "id": 8
}
```

## Step 3: Retrieve the user
To validate the user was added, run the following command. Change the id to match the one returned for your user.

```
curl --location --request GET 'http://localhost:3000/users/8'
```

Now that you have added a user to the To-do service, you can [add a new task for the user](../tutorials/add-a-new-task.md).