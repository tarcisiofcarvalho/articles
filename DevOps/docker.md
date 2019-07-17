# Docker

Usually it is located on:

```sh
/usr/local/bin
```

### Commands

```sh
# Check version
docker --version

# Check the installation
docker run hello-world

# Testing with a webapp
docker run -d -p 80:80 --name webserver nginx

# Check containers
docker container ls
docker ps

# Start/Stop and Remove commands
docker container ls
docker container stop webserver
docker container ls -a
docker container rm webserver
docker image ls
docker image rm nginx

# Pull a image
docker pull <image name as: ibmcom/websphere-traditional>

# Docker stop
docker stop <container>

# Docker remove
docker rm <container>

# Docker list files on container
docker exec <container> ls </dir/path>

```

* It uses **Virtual Machine** for virtualization

Features:

* docker
* docker-compose
* docker-machine

### Docker for Mac

* It uses **hyperkit** for virtualization

Features:

* docker
* docker-compose

