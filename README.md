# Docker files

Project to store personal Docker files with special focus
on database instances.

## TL;DR

To use any instance just go into specific folder and execute the
following command:

```bash
docker compose up -d
```

### Usage example

To use MongoDB instance:

```bash
# Go to mongodb folder
cd mongodb

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

- To remove instance:

```bash
docker compose down

# If you want to remove persisted data
# docker volume rm <DATABASE>_data
docker volume rm mongo_data
```
