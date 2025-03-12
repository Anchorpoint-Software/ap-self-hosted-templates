# Docker Compose Template with Example

In this folder you can find the docker compose parts that are used by the anchorpoint self-hosted cli to create a docker-compose.yml file for your setup.

In the [compose_parts directory](./compose_parts) you can find the various compose yaml parts based on options like http, https, minio or s3 and the traefik setup. Checkout the description in the directory for more information.

The [config directory](./config) contains config files that are volume mounted in the compose parts for the different services of the backend stack. Checkout the descriptionn in the directory for more information.

The [example directory](./example/) contains a finished setup example from the anchorpoint self-hosted cli for a compose setup with a https domain with Let’s Encrypt and minio as s3 provider. Checkout the descriptionn in the directory for more information.