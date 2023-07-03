# WebSpoon instance

This Docker instance will start a Pentaho Spoon web application.
It will create one data volumes `webspoon_pentaho` to store configuration.

In order to remove this instance, run the following commands:

```bash
docker compose down --volumes
```

## UI

WebSpoon will be available in [http://localhost:3080/spoon/spoon](http://localhost:3080/spoon/spoon).

## Data

In order to open and save data inside of the container, a [projects folder](./projects)
has been created. On it you can store all kind of information you
want to open later in WebSpoon. Even if the container is running, you can
add files and they will be visible in the web app.

This folder is not been tracked by Git, so all data will remain in your
machine only.
