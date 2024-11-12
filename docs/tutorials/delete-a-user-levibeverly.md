---
layout: page
---

# Tutorial: Delete a user

Use the following steps to quickly identify and delete a user from your subscriber base. You can perform these steps using [cURL commands](#delete-a-user-with-curl-commands) or in the [Postman application](#delete-a-user-in-postman).

*Note: This tutorial assumes that you have already completed the To-Do Service first-time setup process. If you have not, complete the steps described in [First-time setup](), then return to this tutorial.*

## Delete a user with cURL commands

1. In your preferred command line tool (for new users, we recommend Git Bash), start the To-Do Service locally by entering the following command:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, enter the following GET command to retrieve a complete list of your users:

    ```shell
    curl {base_url}/users
    ```
    *Note: When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.*

    The command line tool returns a complete list of your users.

3. Identify which user you would like to delete. Keep in mind what the user's `id` is; you will need it to run the deletion command. 

4. Enter the following DELETE command. Specify the user you want to delete by replacing `{id}` with the user's `id` at the end of the request.

    ```shell
    curl -X DELETE {base_url}/users/{id}
    ```

    The command line tool returns a message indicating that you successfully deleted the user.
    
    If you want to validate the deletion, re-run the GET command from step 2. The deleted user does not appear in the response body.

## Delete a user in Postman

1. In your preferred command line tool (for new users, we recommend Git Bash), start the To-Do Service locally by entering the following command:

    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following GET request; you will use it to retrieve a complete list of your users:

    ```shell
    GET {base_url}/users
    ```
    *Note: When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.*

4. Click **Send**. 

   Postman returns a `200 OK` message, and the response body lists all your users. 

5. Identify which user you would like to delete. Keep in mind what the user's `id` is; you will need it to run the deletion command.

6. Create the following DELETE request. Specify the user you want to delete by replacing `{id}` with the user's `id` at the end of the request.

    ```shell
    DELETE {base_url}/users/{id}
    ```

7. Click **Send**. 

   Postman returns a `200 OK` message, indicating that you successfully deleted the user.
   
   If you want to validate the deletion, re-run the GET request from step 3. The deleted user does not appear in the response body.

## Learn more

See the following user-related tutorials to learn more about managing your subscriber base:

- [Enroll a new user]()
- [Update an existing user]()
- [Search for users by attribute]()