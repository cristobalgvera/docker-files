# WebSpoon instance

This Docker instance will start a Pentaho Spoon web application.
It will create two data volumes `webspoon_kettle` and `webspoon_pentaho`.

In order to remove this instance, run the following commands:

```bash
docker compose down
docker volume rm webspoon_kettle webspoon_pentaho
```

## UI

Webspoon will be available in [http://localhost:3080/spoon/sponn](http://localhost:3080/spoon/sponn).
