# Featured Repos

* [epm-server](https://hub.docker.com/r/elipsesoftware/epm-server/): EPM Server
* [epm-webserver](https://hub.docker.com/r/elipsesoftware/epm-webserver/): EPM Web Server
* [epm-portal](https://hub.docker.com/r/elipsesoftware/epm-portal/): EPM Portal

# About

[Elipse Plant Manager](https://www.elipse.com.br/en/produto/elipse-plant-manager/) (EPM) is a powerful platform that works as a fundamental vector in the ongoing search for better quality, fewer costs, and higher operational efficiency. With EPM, you can collect data from different sources, store it, and contextualize it; this platform offers high recording and querying performances, in addition to many visualization and analysis tools that speed up your knowledge retrieval process.

Its data handling, compression, and retrieval technologies offer high recording and querying performance, and its visualization and analysis tools provide a collaborative environment for handling information more quickly, reliably and scalably. This allows for the development of industrial intelligence and analysis applications, improving real-time decision making.

# Features
##  Collection

EPM Interface Server is the module responsible for retrieving data at its origin, applying an optional compression algorithm before final storage at EPM Server, which secures data integrity even after a connection shortage (Store and Forward). The available interfaces are [OPC DA](https://opcfoundation.org/about/opc-technologies/opc-classic/), [Elipse Power](https://www.elipse.com.br/en/produto/elipse-power/), and [Elipse E3](https://www.elipse.com.br/en/produto/elipse-e3/), with over 400 I/O drivers available for most devices in the market. There are also database interfaces such as MS SQL Server®, Oracle DB® and others via OLEDB connection.

## Storage and Management

The platform’s main core is EPM Server, responsible for data management and storage as time series, resulting in less disk space cost, high processing capacity and great performance when responding to query requests and writing data. You can also create customized mechanisms for accessing and manipulating data via EPM User API (in .Net) or EPM Python SDK (in expressions or applications developed in Python). These mechanisms allow generating indicators or trends from calculations triggered by value changes or by scheduling. Elipse Plant Manager is also an OPC UA server, allowing real-time and historical series queries via other OPC clients, including user-object definitions, annotations, and event management.

## Analysis and Visualization

EPM Analysis tools allow extracting relevant information from process data, suitable for each organizational level, which makes EPM the right platform in your decision-making process. The most common way of analyzing and visualizing data is via electronic spreadsheets, such as Microsoft Excel using EPM Add-in, but other tools could also be used for this purpose, such as:

* EPM Studio
* [Elipse E3](https://www.elipse.com.br/en/produto/elipse-e3/), [Elipse Power](https://www.elipse.com.br/en/produto/elipse-power/), and EPM Viewer
* DataWeb Parts for Microsoft Sharepoint corporate portal
* [Microsoft SQL Reporting Services’ Reports](https://learn.microsoft.com/en-us/sql/reporting-services) (SSRS)
* [Elipse Mobile](https://www.elipse.com.br/en/produto/elipse-mobile/) (Windows Phone, Android, iOS, Web)
