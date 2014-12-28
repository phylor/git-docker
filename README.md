# Git in Docker

Provides git via SSH in a docker container. Authentication is possible via public keys.

## Run Container

    docker run -p 22:22 -v mypublickey.pub:/keys git

The file located at `/keys` within the container is the
`authorized_keys` file which is used for SSH container. You can either
mount a single public key to it, or a standard `authorized_keys` file.

## Connect via SSH

    ssh git@myserver

### Commands

- `create <repositoryname>` Creates a repository
- `list` Lists all repositories

## URLs to Clone Repositories

    git clone git@myserver:repositoryname
