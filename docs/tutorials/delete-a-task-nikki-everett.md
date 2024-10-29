---
layout: page
---

# Tutorial: Delete a task

In this tutorial, you learn the operations to call to delete a task for a user of the service.

Expect this tutorial to take about 10 minutes to complete. It may take longer if you need to complete prerequisites.

## Before you start

Make sure you've added one or more tasks before attempting to delete a task. For more information, see "[Add a new task](add-a-new-task)".

## Delete a task

Deleting a task from the service requires that you delete (`DELETE`) the [`task`](../api/task.md) resource from the service.

[!WARNING] Deleting a task permanently removes it from the To-Do Service. Always double check the task ID before sending a `DELETE` request.

To delete a task:

1. Make sure your local service is running, or start it by using this command, if it's not.

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new DELETE request. Change the task ID (the number after `tasks/`) to the ID of the task you wish to delete.
    * **METHOD**: DELETE
    * **URL**: `{{base_url}}/tasks/1`

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should be an empty JSON object.

    ```js
    {}
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
