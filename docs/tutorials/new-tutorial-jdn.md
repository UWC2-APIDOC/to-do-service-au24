---
layout: page
---

# Tutorial: Delete a task
There is nothing more satisfying than crossing an item off your to-do list. While you
can't cross off a digital task, you can delete it from your cloud task list.

In this tutorial, you'll learn the operations to delete a task once it is complete (or no longer needed).

Expect this tutorial to take about 10 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md) topic on the development system you'll use for the tutorial.

## Delete a task using curl

To 'DELETE' a task:

1. Make sure your local service is running, or start it by using this command, if it's not.

```shell
cd <your-github-workspace>/to-do-service/api
json-server -w to-do-db-source.json
```

2. Open a separate terminal.

3. To locate the id of the task you'd like to delete, retrieve a list of all tasks.

```shell
curl http://{base_url}/tasks
```

4. Review the returned data to find the unique `id` of the task you'd like to delete.

5. Again, in the terminal, send a `DELETE` call specifying that task `id`

```shell
curl -X DELETE http://{base_url}/tasks/{task-id}
```

6. To verify that the task has indeed been deleted, do another `GET` call for that specific task.

```shell
curl http://{base_url}/tasks/{task-id}
```

If the returned value is a set of empty brackets, your task has been removed from the cloud list.

```
{}
```
However, if the task is returned to you, it is still in the task list. Troubleshoot using the following suggestions, and then repeat steps 5 & 6 again:
    - Verify that you passed the correct task `id` in your `DELETE` call
    - Check that you spelled the commands correctly in your `DELETE' call. For example,
    a common mistake is typing "Delete" instead of "DELETE" in the call.

When the empty brackets are returned to you, you have been successful in deleting your task!

7. Reuse these steps in the future to remove additional completed tasks, and review our [docs](../index.md) to see other
actions you can perform with our API service.
