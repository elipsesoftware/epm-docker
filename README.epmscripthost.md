# Featured Tags

* `latest` (Latest)
  * `docker pull elipsesoftware/epm-scripthost`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPM) Script Host module. This module is required for configuring and running Expression Variables in EPM Server. It is responsible for scheduling and evaluation of python code.

# Configuration

## Environment Variables

You can use environment variables to configure EPM Node on Linux Containers.

- `EPM_SCRIPTHOSTNAME` 
  - The hostname of the machine that is running EPM Server.
- `EPM_SCRIPTHOSTPORT` 
  - The port that EPM Server is using to communicate with EPM Script Host. (Default is 6518)

# Usage

Start an EPM Script Host instance that communicates with an EPM Server at machine (or container) of name epmserver.

> ``docker container run -e "EPM_SCRIPTHOSTNAME=epmserver" -d elipsesoftware/epm-scripthost``

The [EPM Docker samples](https://github.com/elipsesoftware/epm-docker/blob/main/samples) show more ways to configure and use EPM and Docker together.

# Related Repos

EPM:

* [portal](https://hub.docker.com/r/elipsesoftware/epm-portal/): EPM Portal
* [server](https://hub.docker.com/r/elipsesoftware/epm-server/): EPM Server
* [webserver](https://hub.docker.com/r/elipsesoftware/epm-webserver/): EPM Web Server

# Full Tag Listing

## Linux amd64 Tags
Tags | OS Version
-----------| ------------
4.16-alpine3.15, 4.16, latest | Alpine 3.15
4.17-alpine3.15, 4.17, latest | Alpine 3.15