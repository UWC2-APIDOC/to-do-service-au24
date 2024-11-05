---
layout: page
---

# Create your first task
Looking to get your feet wet with the To-Do service API? This quick tutorial
will walk you through creating a reminder task that the API will send to you!

**Time to complete:** 20 minutes or less

## Set up your environment
Before you can create a task, you need to download a few tools and test your development system.

[View this article for these important preliminary steps.](../before-you-start-a-tutorial.md)

**Note:** You only need to follow the setup steps once per development system.

## Add yourself to To-Do service
The best way to learn about the To-Do service is to send a reminder to yourself. In order to do that, you need to add youself as a user to the service.

Open the Postman app on your desktop and complete the following steps:

1. Create a new request with the following values:
- **Method:** POST
- **URL:** {base_url}/users
- **Headers:** Content-Type: application/json

2. Open the **Body** tab
3. Update the following information to your personal details:
```shell
{
  "last_name": "Fountain",
  "first_name": "Jack",
  "email": "j.fountain@example.com",
}
```
4. Select the **Send** button

5. View the JSON response:
```shell
{
    "last_name": "Fountain",
    "first_name": "Jack",
    "email": "j.fountain@example.com",
    "id": 7
}
```

5. Make note of the ID object. You'll need this in the next section when we create the task.

## Create a new reminder task
Now that you have added yourself to the list of users,
you can send yourself a reminder. 

For example, let's say you want to need to mow your grandma's lawn on August 14, 2025 at 2:00pm and you want a reminder one hour before you need to be there.

In Postman, complete the steps below to create that reminder.

1. Create a new request with the following values:
- **Method:** POST
- **URL:** {base_url}/tasks
- **Headers:** Content-Type: application/json

2. Open the **Body** tab 

3. Update the code to match your reminder details. Remember to
inpute the ID number you retrieved when you created yourself as a user.
```shell
  {
      "user_id": 7,
      "title": "Mow the lawn",
      "description": "Mow lawn at Grandma Peggy's house",
      "due_date": "2025-08-14T14:00",
      "warning": "-60"
  }
```

4. Select the **Send** button

5. View the JSON response:
```shell
{
    "user_id": 7,
    "title": "Mow the lawn",
    "description": "Mow lawn at Grandma Peggy's house",
    "due_date": "2025-08-14T14:00",
    "warning": "-60",
    "id": 6
}
```
6. That's it! You should receive your reminder message at the date and time entered.
