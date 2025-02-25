---
title: Docker Setup
---

## Docker Image

The most convenient method of installing and running InvenTree is to use the official [docker image](https://hub.docker.com/r/inventree/inventree), available from docker-hub.

The InvenTree docker image contains all the required system packages, python modules, and configuration files for running a containerised InvenTree web server.

### Tagged Images

Docker images are available with the following tags:

| Tag | Description |
| --- | --- |
| **inventree:stable** | The most recent *stable* release version of InvenTree |
| **inventree:latest** | The most up-to-date *development* version of InvenTree. |
| **inventree:_tag_** | Specific tagged images are built for each tagged release of InvenTree |

### Docker Compose

InvenTree provides sample docker-compose files to get you up and running.

- A *production* compose file is intended to be used in a production environment, running the web server behind a nginx proxy.
- A *development* compose file provides a simple way to spin up a development environment

!!! warning "Docker Compose Version"
    Tthe following guide is designed to work with docker-compose v1.x. There are currently known issues with [docker-compose v2 support](https://github.com/docker/compose/releases/tag/v2.0.0). If you are having issues with the docker installation guide, check the version of docker-compose you are running with the command `docker-compose --version`. 

### Environment Variables

InvenTree run-time configuration options described in the [configuration documentation](./config.md) can be passed to the InvenTree container as environment variables. Using environment variables simplifies setup and improves portability.

### Persistent Data

Persistent data (e.g. uploaded media files) is stored outside the container instance. This directory should be mounted as a volume which the InvenTree docker container can access.

### Configuration File

As discussed in the [configuration documentation](./config.md), InvenTree run-time settings can be provided in a configuration file.

By default, the docker container expects this configuration file in the location `/home/inventree/data/config.yaml`. If this file does not exist, it will be automatically created from a default template file.

As this config file is inside the "data" directory (which should be mounted as a volume) it can be edited outside the context of the container, if necessary.

### Secret Key

InvenTree uses a secret key to provide cryptographic signing for the application.

As specified in the [configuration documentation](./config.md#secret-key) this can be passed to the InvenTree application directly as an environment variable, or provided via a file.

By default, the InvenTree container expects the `INVENTREE_SECRET_KEY_FILE` to exist at `/home/inventree/data/secret_key.txt`. If this file does not exist, it will be created and a new key will be randomly generated.

!!! warning "Same Key"
    Each InvenTree container instance must use the same secret key value, otherwise unexpected behavior will occur.

## Docker Setup Guides

With these basics in mind, refer to the following installation guides:

### Production Server

Refer to the [docker production server setup guide](./docker_prod.md) for instructions on configuring a production server using docker.

### Development Server

Refer to the [docker development server setup guide](./docker_dev.md) for instructions on configuring a development server using docker.
