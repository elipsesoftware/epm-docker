# Featured Tags

* `latest` (Latest)
  * `docker pull elipsesoftware/epmprocessor-workbench`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPMPROCESSOR) Workbench module.

# Configuration

## Requirements

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
- `EPM_PROCESSORENGINEENDPOINT`
  - The endpoint of the EPM Processor Engine REST API module.  
- `EPM_PYTHONSERVICEENDPOINT`
  - The endpoint of the EPM Processor Python Service REST API module.  

# Usage

Start an EPMProcessor Workbench instance using the SA administrator user.

> ``docker container run -e "EPM_AUTHENDPOINT=http://epmwebserver:44333" -e "EPM_WEBAPIENDPOINT=http://epmwebserver:44332" -e "EPM_PROCESSORENGINEENDPOINT=http://epmprocessorengine:44335" -e "EPM_PYTHONSERVICEENDPOINT=http://epmprocessorpyengine:44335" -p 44338:44338 -d elipsesoftware/epmprocessor-workbench``

The [EPM Docker samples](https://github.com/elipsesoftware/epm-docker/blob/main/samples) show more ways to configure and use EPM and Docker together.

# Related Repos

EPM:

* [server](https://hub.docker.com/r/elipsesoftware/epm-server/): EPM Server
* [webserver](https://hub.docker.com/r/elipsesoftware/epm-webserver/): EPM Web Server
* [portal](https://hub.docker.com/r/elipsesoftware/epm-portal/): EPM Portal

# Full Tag Listing

## Linux amd64 Tags
Tags | OS Version
-----------| ------------
4.16-alpine3.15, 4.16, latest | Alpine 3.15
4.17-alpine3.17, 4.17, latest | Alpine 3.17