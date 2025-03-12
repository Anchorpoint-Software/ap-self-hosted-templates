# Docker Compose Template Parts

In this directory you can find the different parts of the docker-compose templates used by the anchorpoint self-hosted cli.

## Base Compose
The base compose contains the setup for the anchorpoint self-hosted container, keycloak as an auth provider and rabbitmq as a message broker.

## Metrics
The metrics stack parts contain setup for grafana, prometheus, loki, promtail, cadvisor, nodeexporter and gets specific overwrites for the three different http setup variants (http, https with Let’s Encrypt, https with own certificate).

## Minio or S3
The minio stack contains setup for the minio container on three different http setup variants (http, https with Let’s Encrypt, https with own certificate). The s3 stack is used if s3 is used instead of minio for storage via the anchorpoint self-hosted cli.

## Traefik
Traefik is the reverse proxy used to access the different exposed containers and also has three setup variants (http, https with Let’s Encrypt, https with own certificate). 

## Env Template
The environment file template that is populated by the anchorpoind self-hosted cli on install command. It generates secrets for various passwords and secret variables.