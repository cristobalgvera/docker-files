# LocalStack instance

This Docker instance will start a LocalStack instance. It will allow you to
run some AWS-related service in local.

If you really want to remove the instance with all persisted data,
then you must run the following command inside this folder:

```bash
docker compose down --volumes
```

## How to use it

LocalStack API Gateway will be located at your localhost in the port
that you defined.
