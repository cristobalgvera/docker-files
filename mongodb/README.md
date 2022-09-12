# MongoDB instance

This Docker compose will create a MongoDB instance that will persist
data inside a volume called `mongodb_data`, meaning that every time
this instance is removed, all the data will be saved and recovered
if the instance is created again.

If you actually want to remove the instance with all persisted data,
then you must run the following command inside this folder:

```bash
docker compose down
docker volume rm mongodb_data
```

## UI

You can go to [http://localhost:8081](http://localhost:8081) and use
the provided interface to query and manage your databases.
