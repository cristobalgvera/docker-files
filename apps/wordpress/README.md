# Wordpress instance

This Docker instance will start a Wordpress web application.
It will create one data volumes `wordpress` and `db` to store configuration.

In order to remove this instance, run the following commands:

```bash
docker compose down --volumes
```

## UI

Wordpress will be available in [http://localhost:8080](http://localhost:8080).

## Custom configurations

You can copy any file located in the `config` directory by doing the following:

```bash
cd config
cp <file-name>.example <file-name>
# E.g.: cp .htaccess.example .htaccess
```

This will allow you to customize the Wordpress instance. Feel free to modify the
`config` directory to your needs.
