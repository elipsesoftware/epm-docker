# Featured Tags

* `latest` (Latest)
  * `docker pull elipsesoftware/epm-node`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPM) Node module. This module is required for EPM Portal to run and is responsible for theming generation and all Widget development and build related flow: compilation of SASS and Typescript code, generation of web fonts, minification and bundling of compiled code, and so on...

# Configuration

## Environment Variables

You can use environment variables to configure EPM Node on Linux Containers.

- `EPM_NODEPORT` 
  - The port where the EPM Node server will be listening on. (Default is random)

# Usage

Start an EPM Node instance using the SA administrator user.

> ``docker container run -e "EPM_NODEPORT=46000" -d elipsesoftware/epm-node``

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