# Config Volume Mounts
This folder contains the volume mounts that the anchorpoint self-hosted cli uses. The paths are set in the environment file of the folder.

## Grafana
Grafana has default dashboards descriptions as yaml / json files. You can find more infos about the dashboards in the self-hosted documentation [here](https://docs.anchorpoint.app/docs/general/faq/self-hosting/metrics/#dashboards-overview). Datasources defines the grafana access for prometheus and loki services running in the stack.

## Keycloak
Keycloak contains the `anchorpoint-realm.json` that is loaded by the keycloak container on startup to make sure that the anchorpoint realm exists in the keycloak database.

Note that the cli changes `"secret": "adminCliSecret"` and `"secret": "adminWebSecret"` in the `anchorpoint-realm.json` to random generated secrets.

The themes folder contains an anchorpoint theme which overwrites the login theme for the anchorpoint realm. The theme is set in the `anchoroint-realm.json` via `"loginTheme": "anchorpoint"`.

## Loki
The loki configuration defines retention periods and other loki specific configurations and also contains the promtail config.

## Postgres
The postgres config folder contains a script to create multiple databases on launch of the postgres container. It is run by the postgres compose and reads the `POSTGRES_MULTIPLE_DATABASES: keycloak,${POSTGRES_DB}` environment variable and creates a database `keycloak` and on default a database named `ap` from the `${POSTGRES_DB}` environment file.

Note if you want to use your own postgres server make sure that both databases are available and accessable via the `POSTGRES_` variables from the environment file.

## Prometheus
The prometheus config contains the scrape configuration for the other metrics services that are running in the stack.

## Traefik
This folder holds a dynamic configuration which needs to be used for setting a custom ssl certificate. You can read more about this custom certificate setup [here](https://docs.anchorpoint.app/docs/general/faq/self-hosting/server-setup/#how-to-use-your-own-ssl-certificates)