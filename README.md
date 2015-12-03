# Clustered NodeJS for Docker

This is an example project for running [nodejs](https://nodejs.org/) in two [docker](https://www.docker.com/) containers and using [nginx](http://nginx.org/) as load balancer.

The application used in this docker image is [nodejs-example](https://github.com/mrako/nodejs-example).

## Building

    docker-compose build

## Starting

    docker-compose up

## Connecting to docker images

    docker ps
    docker port <container id>
    docker-machine ip default

    curl -i <machine ip>:<docker port>

## Single containers

### Building

    docker build .

### Running

    docker run -P -d <image id>
    docker run -p 8080:8080 -d <image id>

### Running interactively

    docker run -ti <image id> bash
