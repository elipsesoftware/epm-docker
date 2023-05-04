# EPM and Nginx Docker Sample

This sample demonstrates how to run an EPM solution behind an Nginx reverse proxy. Only the Nginx server and EPM Server are exposed and publicly accessible from outside the containers.

All the containers are orchestrated using a Docker Compose YAML [file](https://github.com/elipsesoftware/epm-docker/blob/main/samples/docker-compose.yml). The configuration of the containers are done using an .env [file](https://github.com/elipsesoftware/epm-docker/blob/main/samples/.env).

The instructions assume that you have cloned this repo, have [Docker](https://www.docker.com/products/docker) installed, and have a command prompt open within the `samples/nginx` directory within the repo.

## Starting the application

Before starting the application, update the IP address of all `extra_hosts` properties of the Docker Compose YAML [file](https://github.com/elipsesoftware/epm-docker/blob/main/samples/docker-compose.yml) so that the `localhost:[localhost IP]` matches the actual IP address of the host machine.

```
extra_hosts:
  - "localhost:[localhost IP]"
```

You can start the application running the following command, which will run all the containers declared in the YAML file:

```
docker-compose up
```

Wait some time until the application starts.

> Note: The compose [file](https://github.com/elipsesoftware/epm-docker/blob/main/samples/docker-compose.yml) maps ports 8181 and 443 (HTTPS) on your local machine to port 8181 and 443 (HTTPS) in the nginx container. See the [Docker Compose file reference](https://docs.docker.com/compose/compose-file/compose-file-v3/#ports) for more information. In some cases, you might see an error because the host port you select is already in use. Choose a different port in that case.

You can navigate do https://localhost in your web browser to connect to the EPM Portal container.

Also, you can [download](https://www.elipse.com.br/en/downloads) and install EPM Studio to access the EPM Server container that is running as part of this sample.

## Stopping the application

You can stop the running containers using the following command:

```
docker-compose down
```

Wait some time until the application containers stops.