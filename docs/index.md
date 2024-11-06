---
layout: page
---

# To-Do service API

This is a mock API to simulate the REST interface of an
imaginary service.

The To-Do service provides a cloud-hosted task list through which
subscribers can post tasks and receive reminders of those tasks.

## Quickstart

[Emroll your first user](tutorials/first-use-alicia.md) with the To-Do service to learn how to get started. 

## Tutorials

Learn how to do common tasks with in the To-Do service.

First, do this tutorial to set up your development system for these tutorials. You only have to do this one time per development system.

* [Before you start a tutorial](before-you-start-a-tutorial.md)

After your system is ready, these tutorials show you how to perform common tasks.

* [Enroll a new user](tutorials/enroll-a-new-user.md)
* [Add a new task](tutorials/add-a-new-task.md)
* [Change the due-date of a task _(coming soon)_](#tutorials)
* [Delete a task _(coming soon)_](#tutorials)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When run locally for testing, the `{base_url}` is
generally `http://localhost:3000`.

* [user resource](api/user.md)
* [task resource](api/task.md)
