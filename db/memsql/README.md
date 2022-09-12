
# MemSQL instance

This Docker compose will create a MemSQL instance that will persist
data inside a volume called `memsql_data`, meaning that every time
this instance is removed, all the data will be saved and recovered
if the instance is created again.

If you actually want to remove the instance with all persisted data,
then you must run the following command inside this folder:

```bash
docker compose down
docker volume rm memsql_data
```

## UI

You can go to [http://localhost:8080](http://localhost:8080) and use
the provided interface to query and manage your databases. To enter,
you just need to set username as `root` and leave password field blank.

Also, you can use API in port 9000.
