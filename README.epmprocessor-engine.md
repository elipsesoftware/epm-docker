# Featured Tags

* `latest` (Latest)
  * `docker pull elipsesoftware/epmprocessor-engine`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPMPROCESSOR) Engine module.

# Configuration

## Requirements

- At least 4 GB of RAM
- 400MB of disk space

## Environment Variables

You can use environment variables to configure EPM Web Server on Linux Containers.

- `EPM_AUTHENDPOINT`
  - The endpoint of the Elipse Plant Manager (EPM) Web Server authentication module.
- `EPM_WEBAPIENDPOINT`
  - The endpoint of the Elipse Plant Manager (EPM) Web Server REST API module.
- `EPM_PYTHONSERVICEENDPOINT`
  - The endpoint of the EPM Processor Python Service REST API module.  
- `EPM_MONGODBENDPOINT`
  - The endpoint of the Processor Database MongoDB Service module.  
- `EPM_EPMUSER`
  - The username that will be used to connect to the EPM Server. This user MUST be part of the AdminGroup.
- `EPM_EPMPWDPLAIN`
  - The password of the EPM user.
- `EPM_MONGOADMPASSWORDPLAIN`
  - The password of the admin user from Processor Database MongoDB Service.
- `EPM_METHODEXECUTIONTIMEOUT`
  - The timeout from EPM Processor calculations in minutes.
  
  


# Usage

Start an EPMProcessor Engine instance.

> ``docker container run -e "EPM_AUTHENDPOINT=http://epmwebserver:44333" -e "EPM_WEBAPIENDPOINT=http://epmwebserver:44332" -e "EPM_PYTHONSERVICEENDPOINT=http://epmprocessorpyengine:44335" -e "EPM_MONGODBENDPOINT=mongodb://epmprocessordatabase:44337" -e "EPM_EPMUSER=user" -e "EPM_EPMPWDPLAIN=xxxx" "EPM_MONGOADMPASSWORDPLAIN=xxxx" -p 44336:44336 -d elipsesoftware/epmprocessor-engine``

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