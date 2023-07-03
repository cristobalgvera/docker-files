# DynamoDB instance

This Docker compose will create a DynamoDB instance that will persist
data inside a folder called `data`, that will be created after your first run,
meaning that every time this instance is removed, all the data will be
saved and recovered if the instance is created again.

If you actually want to remove the instance with all persisted data,
then you must run the following command inside this folder:

```bash
docker compose down
rm -rf data
```

## UI

You can go to [http://localhost:8001](http://localhost:8001) and use
the provided interface to query and manage your database.

## AWS CLI

In order to run a custom `aws-cli` command against the dynamodb container,
you have to follow these steps:

1. Write the command you want to run in the `command` entry below the `aws-cli`
   service inside the [compose.yml](./compose.yml) file. It will prepends a `aws`
   to your command.

   This custom command:

   ```bash
   services:
     # Other services...
     aws-cli:
       command: dynamodb list-tables --endpoint-url http://dynamodb:8000
       # Other configurations...
   ```

   Will be executed inside the container as:

   ```bash
   aws dynamodb list-tables --endpoint-url http://dynamodb:8000
   ```

1. Run the `aws-cli` service.

   ```bash
   docker compose up aws-cli
   ```
