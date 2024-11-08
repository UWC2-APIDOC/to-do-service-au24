# Tutorial: Delete a task

Here you will learn here how to delete a task from your to-do list.

This tutorial takes about 10 minutes to complete.

**Caution**: Deleting a task removes the task item from the To-do Service forever.

## Prerequisites

Make sure to complete all of the steps in [System Pre-requisites](../before-you-start-a-tutorial.md).

## Delete a task

Deleting a task uses a request with the (`DELETE`) method and the task's task ID.

### To delete a task

1. Confirm your local service is running. If it's not, use the following command to start it:

    ```shell
    cd your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

2. Open the Postman app on your desktop.
3. In the Postman app, create a new request with the following values:
   * **METHOD**: DELETE
   * **URL**: `{{base_url}}/tasks`
   * **ID**: {ID number for the task you want to delete}
       * **Tip**: Complete a Get All Tasks request to retrieve all your task IDs.
   * **Example request URL**: `http://localhost:3000/tasks/6`
4. In the Postman app, choose **Send** to complete the request.
5. Your response body will be empty because there is no information to return.

## Confirm the deletion

Verify your request was successful by sending a GET All Tasks request to check that your task no longer appears as a response.

## Related pages
* [Add a new task](add-a-new-task.md)
