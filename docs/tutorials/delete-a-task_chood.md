# Tutorial: Delete a task

Here you will learn here how to delete a previously created task from your to-do list.

This tutorial will take about 10 minutes to complete.

**Caution**: Deleting a task will remove the task item from the To-do Service forever.

## Pre-requisites

Make sure you have completed all of the steps in [System Pre-requisites](../before-you-start-a-tutorial.md) before you start the tutorial.

## Delete a task

Deleting a task requires you add (`DELETE`) to a task request with a specific task ID.

### To delete a task

1. First ensure your local service is running. If not, you can start it using the following command:

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
* [Add a new task](..//tutorials/add-a-new-task.md)
* GET All Tasks