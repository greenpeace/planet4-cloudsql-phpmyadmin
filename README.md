# Connects phpmyadmin to Google CloudSQL

## Usage:

Create a `db.env` in the `secrets` directory with authentication details like so:

```
MYSQL_USER=<database username>
MYSQL_PASSWORD=<database password>
MYSQL_DATABASE=<database name>
```

Obtain the service account json file and save it in the `secrets` directory as `cloudsql-service-account.json`. For instructions on creating or obtaining a CloudSQL service account see: https://cloud.google.com/sql/docs/mysql/connect-docker#connect-client

Configure the CloudSQL instance parameters via environment variables:

| Variable      | Default                |
|---------------|------------------------|
| CLOUDSQL_NAME | planet4-gpi-production |
| PROJECT       | planet4-gpi            |
| REGION        | us-central1            |


Start the containers with `docker-compose up`.

Example:
```
CLOUDSQL_NAME=planet4-test PROJECT=planet-4-151612 REGION=us-west1 docker-compose up
```


Open your browser to http://localhost:8008
