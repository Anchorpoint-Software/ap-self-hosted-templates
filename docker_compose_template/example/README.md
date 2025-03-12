# Example
The example is based on the output from the anchorpoint self-hosted cli and provides an example for a https (with Let’s Encrypt) based anchorpoint self-hosted stack with minio as s3 storage, a postgres container and the metrics stack with grafana, prometheus and loki.

The secrets in the [env file](./.env) are changed to placeholders, but the rest of the environment file shows the setup correctly.

The [docker-compose.yaml file](./docker-compose.yaml) shows the combined, generated docker-compose generated from the according parts from [compose_parts](./../compose_parts)
