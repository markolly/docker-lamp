# LAMP for Docker
A clustered LEMP example running on Docker. Contains 2 node Apache cluster with PHP and MySQL served by Traefik proxy/LB.

## Prerequisites
The following software is required before running LEMP for Docker:
- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Install
To build and start the complete stack simply run the following:
```
$ git clone git@github.com:markolly/docker-lamp.git
$ cd docker-lamp
$ docker-compose up -d
```
Containers can be checked for their current state by running:
```
$ docker ps
```

## Accesing sites
Traefik has been set up to use name-based virtual hosting. Once the stack is up and running sites will be available at the following locations:

-  Traefik LB - http://traefik.docker.localhost
-  Apache site - http://apache.docker.localhost
-  phpMyAdmin - http://pma.docker.localhost (Server:mysql, Username:project, Password:project)

## Updating a container
The majority of the images used in the stack are pulled straight from Docker Hub apart from the Apache container. This is built using a Dockerfile located at docker/php/Dockerfile. 

## Uninstall
To stop all "LAMP for docker" containers and delete them run: 
```
$ docker-compose down 
```
