Atlassian Jira System in Docker images
===========================

### Description

This repository stores Atlassian project management system organized in Docker containers, which is started with a minimum number of commands and in one place. It can be useful for developers of add-ons to Atlassian applications, testers, as well as analysts, to demonstrate the capabilities of the Atlassian products to end users.

The system consists of the following set of containers:

* _Jira_ - Task management application.
* _PostgreSQL_ - database management system for Atlassian apps.
* _Nginx_ - Reverse proxy web server for web applications which to forward ports to the host system, as well as mount the prepared configuration file and event logs.
* _Prometheus_ - Monitoring tool which is responsible for collecting and storing metrics. The paths and methods of the received metrics were written in the _Prometheus.yml_ configuration file, that mounted to the container.
* _Grafana_ - Data visualization web application. The panel with server monitoring will allow to display such data as: server uptime, CPU load, memory usage, disk space and capacity of network interfaces.

The whole system starts from one _docker-compose.yml_ file withthe internal Docker network for the interaction of containers with each other.