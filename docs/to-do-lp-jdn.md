---
layout: page
---

# Overview of the To-Do service API

This is a mock API to simulate the REST interface of an
imaginary service.

The To-Do service provides a cloud-hosted task list through which
subscribers can post tasks and receive reminders of those tasks.

## Quickstart

[Post your first task _(coming soon)_](#quickstart) with the To-Do service to see how easy it is to use!

## Prerequisites

Use these instructions to set up your development system to run the following tutorials. You only have to do this one time per dev system.

* [Set up your dev system](before-you-start-a-tutorial.md)

## Tutorials

Once your dev system is ready, use these tutorials to learn how to perform common tasks with the To-Do service.

* [Enroll a new user](tutorials/enroll-a-new-user.md)
* [Add a new task](tutorials/add-a-new-task.md)
* [Change the due-date of a task _(coming soon)_](#tutorials)
* [Delete a task _(coming soon)_](#tutorials)

## To-Do service API reference docs

Find detailed descriptions of this service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.

* [User resource overview](api/user.md)
    * [Get all users](api/users-get-all-users.md)
    * [Get users by ID](api/users-get-user-by-id.md)
* [Task resource overview](api/task.md)
    * [Get all tasks _(coming soon)_](#resource-properties)
    * [Get task by ID _(coming soon)_](#resource-properties)
    * [Get task by user ID _(coming soon)_](#resource-properties)
