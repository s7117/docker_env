# Ubuntu 20.04 Docker Development Environment
*** Be sure to change the password for the user and root immediately after creating the container! ***

## Configuration/Installation
1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop).
1. Start the Docker Daemon by searching for the program and starting it. It is useful to have docker always startup on login.
1. Run ```docker pull s7117/ubuntu_env```
1. Run ```docker run --name <container_name> --hostname <hostname> -ti s7117/ubuntu_env```

## Enter the shell via `docker exec` or `docker start`
- `docker start -ai <container_name>`
- `docker exec -u user -w /home/user -ti  <container_name> /bin/zsh`
- `docker exec <container_name> <executable>`

Optionally, you can add the ```--restart unless-stopped``` to the ```docker run``` command to restart the docker container on docker startup.