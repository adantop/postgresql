# PostgreSQL Deployment

This deployment comes with PGAdmin 4, it requires two volumes to work **pg-data** which stores databases data and **pgadmin-data** which stores pgadmin user data. Common environment variables can be set in an env file; there is a sample config file in this repository: `config/local.env`

## Useful commands

1. Create volumes (once)

    ```shell
        docker volume create pg-data
        docker volume create pgadmin-data
    ```

1. Run with Docker Compose

    ```shell
        cd <project root>
        docker-compose --env-file ./config/local.env up -d
    ```

1. Delete the deployment

    ```shell
        cd <project root>
        docker-compose down
    ```

