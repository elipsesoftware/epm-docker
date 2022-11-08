# Featured Tags

* `4.15-latest` (Latest)
  * `docker pull elipsesoftware/epm-portal:4.15`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPM) Portal module.

# Configuration

## Requirements

- Windows Server 2012 R2
- At least 4 GB of RAM
- 400MB of disk space

## Environment Variables

You can use environment variables to configure EPM Web Server on Linux Containers.

- `EPM_SERVERPORT` 
  - The port where the EPM Portal server will be listening on. (Default is 44331)
- `EPM_AUTHENDPOINT`
  - The endpoint of the Elipse Plant Manager (EPM) Web Server authentication module.
- `EPM_WEBAPIENDPOINT`
  - The endpoint of the Elipse Plant Manager (EPM) Web Server REST API module.
- `EPM_NODEENDPOINT`
  - The endpoint of the Elipse Plant Manager (EPM) Node server.
- `EPM_CORSALLOWEDORIGINS`
  - A list of URLs that are allowed to make cross origin requests.

# Usage

Start an EPM Portal instance using the SA administrator user.

> ``docker container run -e "EPM_AUTHENDPOINT=http://epmwebserver:44333" -e "EPM_WEBAPIENDPOINT=http://epmwebserver:44332" -e "EPM_NODEENDPOINT=http://epmnode:46000" -p 44331:44331 -d elipsesoftware/epm-portal``

The [EPM Docker samples](https://github.com/elipsesoftware/epm-docker/blob/main/samples/README.md) show more ways to configure and use EPM and Docker together.

# Related Repos

EPM:

* [server](https://hub.docker.com/r/elipsesoftware/epm-server/): EPM Server
* [webserver](https://hub.docker.com/r/elipsesoftware/epm-webserver/): EPM Web Server

# Full Tag Listing

## Linux amd64 Tags
Tags | OS Version
-----------| ------------
4.16-alpine3.15, 4.16, latest | Alpine 3.15