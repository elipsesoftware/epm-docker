# Featured Tags

* `latest` (Latest)
  * `docker pull elipsesoftware/epm-server`

# About

This image contains the [Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPM) Server module.

# Configuration

## Requirements

- Windows Server 2012 R2
- At least 8 GB of RAM
- 250MB of disk space
- Microsoft SQL Server 2012

## Environment Variables

You can use environment variables to configure EPM Server on Linux Containers.

- `EPM_DATABASECONNECTIONSTRING` 
  - The string that will be used to connect to the database source.
- `EPM_DATABASENAME`
  - The name of the database where the EPM data is located.
- `EPM_ADMINPASSWORD`
  - The EPM administrator password that will be used by the server.
- `EPM_CONFIGUREDATABASE`
  - Performs the creation or an upgrade of an EPM Database before running the server.
- `EPM_INTERFACESERVERACTIVITYTIMEOUT`
  - How long the communication with the EPM Interface Server will take before receiving timeout messages.
- `EPM_CONSUMECACHEINTERVAL`
  - The interval of consuming and storage of cached value messages.

# Usage

Start an EPM Server instance that will create a new EPM Database before initialization.

> ``docker container run -e "EPM_DATABASECONNECTIONSTRING=Data Source=database;Integrated Security=False;User ID=sa;Password=yourStrongDB(!)Password" -e "EPM_DATABASENAME=EpmDatabase" -e "EPM_ADMINPASSWORD=yourStrong(!)Password" -e EPM_CONFIGUREDATABASE=TRUE -p 6516:6516 -d elipsesoftware/epm-server``

The [EPM Docker samples](https://github.com/elipsesoftware/epm-docker/blob/main/samples) show more ways to configure and use EPM and Docker together.

# Questions 
- **How do I map a volume using Docker for Windows?** Make sure to enable [shared drives in the settings menu](https://docs.docker.com/docker-for-windows/#shared-drives). After that, you can map a volume specifying the **Windows path:Linux path**. The following is an example of a command to map a Windows folder to the ProgramData directory in the container:

> ``docker run -v "${PROGRAMDATA}/Elipse Software/EpmServer:/usr/share/Elipse Software/EpmServer" -e "EPM_DATABASECONNECTIONSTRING=Data Source=database;Integrated Security=False;User ID=sa;Password=yourStrongDB(!)Password" -e "EPM_DATABASENAME=EpmDatabase" -e "EPM_ADMINPASSWORD=yourStrong(!)Password" -p 6516:6516 -d elipsesoftware/epm-server``


# Related Repos

EPM:

* [portal](https://hub.docker.com/r/elipsesoftware/epm-portal/): EPM Portal
* [webserver](https://hub.docker.com/r/elipsesoftware/epm-webserver/): EPM Web Server

# Full Tag Listing

## Linux amd64 Tags
Tags | OS Version
-----------| ------------
4.16-alpine3.15, 4.16, latest | Alpine 3.15