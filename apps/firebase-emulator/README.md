# Firebase Emulator instance

This Docker compose will create a Firebase Emulator instance that will persist
data inside a volume called `firebase-emulator_data`, meaning that every time
this instance is removed, all the data will be saved and recovered if the instance
is created again.

If you actually want to remove the instance with all persisted data,
then you must run the following command inside this folder:

```bash
docker compose down --volumes
```

## UI

You can go to [http://localhost:4000](http://localhost:4000) and use
the provided interface to manage the emulator.
