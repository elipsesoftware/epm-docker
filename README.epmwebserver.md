# Featured Tags

* `latest` (Latest)
  * `docker pull elipsesoftware/epm-webserver`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPM) Web Server module.

# Configuration

## Requirements

- Windows Server 2012 R2
- At least 2 GB of RAM
- 400MB of disk space

## Environment Variables

You can use environment variables to configure EPM Web Server on Linux Containers.

- `EPM_AUTHPORT` 
  - The port where the EPM authentication server (OAuth) will be listening on. (Default is 44333)
- `EPM_WEBAPIPORT` 
  - The port where the server of all EPM related REST API will be listening on. (Default is 44332)
- `EPM_WEBAPIDOC` 
  - Enables the Swagger documentation endpoint of the EPM REST API.
- `EPM_EPMSERVER`
  - The endpoint of the Elipse Plant Manager (EPM) Server.
- `EPM_EPMUSER`
  - The username that will be used to connect to the EPM Server. This user MUST be part of the AdminGroup.
- `EPM_EPMPWD`
  - The password of the EPM user.
- `EPM_PORTALREDIRECT`
  - A list of allowed URLs that users can redirected to as part of the EPM Portal authentication flow (OAuth).
- `EPM_PROCESSORREDIRECT`
  - A list of allowed URLs that users can redirected to as part of the EPM Processor Workbench authentication flow (OAuth).

# Usage

Start an EPM Web Server instance using the SA administrator user.

> ``docker container run -e "EPM_EPMSERVER=epmserver" -e "EPM_EPMUSER=sa" -e "EPM_EPMPWD=yourStrong(!)Password" -p 44332:44332 -p 44333:44333 -d elipsesoftware/epm-webserver``

The [EPM Docker samples](https://github.com/elipsesoftware/epm-docker/blob/main/samples) show more ways to configure and use EPM and Docker together.

# Related Repos

EPM:

* [server](https://hub.docker.com/r/elipsesoftware/epm-server/): EPM Server
* [portal](https://hub.docker.com/r/elipsesoftware/epm-portal/): EPM Portal

# Full Tag Listing

## Linux amd64 Tags
Tags | OS Version
-----------| ------------
4.16-alpine3.15, 4.16, latest | Alpine 3.15