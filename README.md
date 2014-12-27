# Git in Docker

Provides git via SSH in a docker container. Authentication is possible via public keys.

## Run Container

    docker run -p 22:22 -v mypublickey.pub:/home/git/.ssh/authorized_keys git

## Connect via SSH

    ssh git@myserver

### Commands

- `create <repositoryname>` Creates a repository
- `list` Lists all repositories

## URLs to Clone Repositories

    git clone git@myserver:repositoryname
