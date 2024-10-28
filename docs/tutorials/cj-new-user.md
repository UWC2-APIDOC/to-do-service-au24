# Tutorial: Enroll a new user


Using this tutorial, you will add (`POST`) the details of a new [`user resource`](../api/user.md) to the service, enrolling a new user!

This should take about **15 minutes** to complete.

## Before you start

1. Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md) topic. This will ensure your development system is running correctly!
2. Start your local service if it isn't already running by using the following command:
    ```shell
    cd <your-github-workspace>/to-do-service/api
    json-server -w to-do-db-source.json
    ```

## Let's get started


1. Using the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/users`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        Please reference the [`user resource page`](../api/user.md) for a guide to each property.

        ```js
        {
            "last_name": "Jones",
            "first_name": "Jenny",
            "email": "jen.jones@example.com"
        }
        ```

3. Click **Send** to make the request!
   * Observe the response body. The `last_name`, `first_name`, and `email` values should remain as what you entered in **Step 2**, and there should be a new `id` value.

    ```js
    {
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com",
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
