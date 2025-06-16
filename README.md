n8n with PostgreSQL
===================

Starts n8n with PostgreSQL as database.

Setup Instructions
-----
1. Get ngrok authtoken
    - Sign up at [ngrok.com](https://ngrok.com)
    - Go to your dashboard and copy your authtoken
    - Add it to the .env file

2. Start

    To start n8n with PostgreSQL simply start docker-compose by executing the following command in the current folder.

    IMPORTANT: But before you do that change the default users and passwords in the [`.env`](https://github.com/posheng/n8n-postgres/blob/main/.env) file!

    ```
    docker-compose up -d
    ```

    To stop it execute:

    ```
    docker-compose stop
    ```

3. Find your ngrok URL
    - Visit `http://localhost:4040` to see the ngrok web interface
    - Copy the HTTPS URL (e.g.,` https://abc123.ngrok.io`)

4. Update the webhook URL
    - Edit the `.env` file
    - Replace `https://your-ngrok-url.ngrok.io/` with your actual ngrok URL
    - Restart n8n: `docker-compose restart n8n`

Configuration
-------------

The default name of the database, user and password for PostgreSQL can be changed in the [`.env`](https://github.com/posheng/n8n-postgres/blob/main/.env) file in the current directory.
