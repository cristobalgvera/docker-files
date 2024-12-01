# Wordpress instance

This Docker instance will start a Wordpress web application.
It will create one data volumes `wordpress` and `db` to store configuration.

In order to remove this instance, run the following commands:

```bash
docker compose down --volumes
```

## UI

Wordpress will be available in [http://localhost:8080](http://localhost:8080).
