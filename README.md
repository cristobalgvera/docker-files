# Docker files

Project to store personal Docker files with special focus
on database instances.

## TL;DR

To use any instance just go into specific folder, fill `.env` file with
your specifications following the `.env.example` file located on each folder
and then execute the following command:

```bash
docker compose up -d
```

### Usage example

To use MongoDB instance:

```bash
# Go to MongoDB folder
cd db/mongodb

# Copy .env.example file into a .env file
cp .env.example .env

# Fill .env variables
vim .env

# Create the container
docker compose up -d
```

Then, inside `mongodb` folder, run any of the following commands:

- To stop started instance:

```bash
docker compose stop
```

- To start stopped instance:

```bash
docker compose start
```

- To remove instance: _(each folder has instructions to remove his instance)_

```bash
docker compose down

# If you want to remove persisted data
# docker compose down --volumes
```
