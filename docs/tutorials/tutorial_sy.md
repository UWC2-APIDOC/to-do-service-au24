---
layout: page
---

# Tutorial: Change the due-date of a task

In this tutorial, you change the due-date of a task in the To-Do service.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

1. Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md) topic on the development system that you'll use for the tutorial.

2. Make sure that a task already exists in the service or add a new task as described in the [Add a new task tutorial](add-a-new-task.md). You'll need the `id` of the [`task`](../api/task.md) resource that you want to change.

## Change a task's due-date

Changing a task's due-date requires that you `PATCH` the `due_date` property of a [`task`](../api/task.md) resource.

To change the task's due-date:

1. In a command-line tool, start your local To-Do service by using this command, if it's not already running.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. In another command-line window, run this command to make a `PATCH` request. Substitute:

    * `<date>` with the new due-date in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.
    * `<id>` with the `id` of the task that you want to change.

    ```shell
    curl -d "due_date=<date>" -X PATCH http://localhost:3000/tasks/<id>
    ```

    For example, if you want to change the due-date of task `1` to `2024-10-28T14:00`, run:

    ```shell
    curl -d "due_date=2024-10-28T14:00" -X PATCH http://localhost:3000/tasks/1
    ```

3. The command returns the response body, which should include the same `id` as the task you changed, as well as the updated `due_date` value. For example, if you changed task `1` to have a due-date of `2024-10-28T14:00`, the response might look like:

    ```js
    {
      "user_id": 1,
      "title": "Grocery shopping",
      "description": "eggs, bacon, gummy bears",
      "due_date": "2024-10-28T14:00",
      "warning": "-10",
      "id": 1
    }
    ```

After completing this tutorial using cURL, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
