---
layout: page
---

# To-Do service API

Still using that old pad of sticky notes to keep track of what you need to do and when? Leave that old way of reminders in the past with the To-Do service API!

## What it is

The To-Do service is a cloud-hosted task list that allows
subscribers to post tasks and receive reminders of those tasks through an email message.

## How it works

For example, let's say you need to buy milk and eggs at the grocery store on Friday morning. You could add a task to the To-Do service that includes a task title (groceries), description (milk and eggs), due date and time (Friday at 9:00am), and when you want to receive your reminder (15 minutes before). At 8:45 on Friday, you would receive an email reminder to buy milk and eggs.

The groceries are taken care of and you don't have to eat candy bars for breakfast!
(unless you want to - no judgement here.)

## Set up your development system

Before you dive into our tutorials and start loving the To-Do service, you need to set up your system so everything runs smoothly. View the article below for detailed steps:

- [Set up your development system](before-you-start-a-tutorial.md)

**Note:*- You only need to follow the setup steps once per development system.

## Create your first task

Ready to give the To-Do service a spin? Find a quick guide below for steps on creating your first task.
We're sure you'll be surprised at how easy it is to use.

- [Create your first task](tutorials/create_first_task_CT.md)

## Tutorials

Through the To-Do service, you can easily update task reminders and the list
of users who receive them. View the tutorials below for more information.

### Tasks

- [Add a new task](tutorials/add-a-new-task.md)

### Users

- [Enroll a new user](tutorials/enroll-a-new-user.md)
- [Get a user by their user ID](api/users-get-user-by-id-CT.md)

## API reference docs

The To-Do service relies on two basic endpoints: task (the To-Do reminder)
and user (the individual reminded about task). Learn more about these endpoints by reviewing the resources below.

- [Task resource](api/task.md)
- [User resource](api/user.md)

### Base URL

The API reference docs refer to a `{base_url}` for the URL of a resource.
The `{base_url}` value depends on the installation of the service. When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.
