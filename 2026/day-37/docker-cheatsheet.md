# Docker Commands Cheat Sheet

### Container commands


| Command | Description |
|------|----------|
| docker run | docker run command runs the image (ex. nginx,etc) |
| docker run -d <image_name> | runs the particular image in detached mode |
| docker run -p 80:80 <image> | Add port mapping |
| docker run -e MYSQL_ROOT_PASSWD=root mysql | Add environment variable |
| docker run -v mysql:/var/lib/mysql mysql | Add volume |
| docker ps | docker ps shows the list of running container | 
| docker ps -a | lists all the container |
| docker stop | stops the running container | 
| docker stop $(docker ps -q) | Stop all containers |
| docker restart <container_id> | Restart a container |
| docker kill <container_id> | Kill a container |
| docker rm <container_id> | Remove a container |
| docker rm -f <container_id> | Remove a running container|
| docker rm $(docker ps -aq) | Remove all stopped container |
| docker exec -it <container_id> bash | Get into a container by its id in bash shell |
| docker exec <container_id> ls /pp | Run a single command inside container |
| docker logs <container_id> | View logs of a container |
| docker inspect <container_id> | Inspect a container |

### Image commands 

| Command | Description |
|------|----------|
| docker build -t <image_name> . | Builds an imagefor dockerfile | 
| docker build -t <image_name> . -no-cache | buids an image from a Dockerfile without the cache |
| docker  pull <image_name> | pull an image  |
| docker  push <image_name> | push an image  |
| docker rmi <image_name> | Remove image |
| docker  image prune | Remove unused image  |
| docker  image inspect <image_id> | Inspect an image |

### Network commands

| Command | Description |
|------|----------|
| docker network ls | list networks |
| docker network create <name> | create network |
| docker network create --driver bridge <name> |  create a network with specified driver |
| docker network rm <name> | remove network |
| docker network inspect <name> | inspect network |
| docker network prune | remove unused network |

### Compose commands

| Command | Description |
|------|----------|
| docker compose up | run docker compose services |
| docker compose down | stop&remove all |
| docker compose stop | stop all |
| docker compose up -d | run in detached mode |
| docker compose ps | view all |
| docker compose logs | view all logs |
| docker compose up --build | build again, dont use cache |
| docker compose restart | restart all |

### Cleanup commands

| Command | Description |
|------|----------|
| docker system prune | removed unused networks, stopped containers, dangling images, unused build cache |
| docker system prune -a | evrything above + unused images |

### Dockerfile instructions

| Command | Description |
|------|----------|
| FROM | use a base image |
| RUN | to run commands during image build |
| COPY | copy from host to container |
| WORKDIR | set working directory inside container |
| EXPOSE | declares the port the container listens on, but does not publish it |
| CMD | default command to run when container is spin up, can be overridden with docker run aruguments  |
| ENTRYPOINT | default command to run when container is spin up, can be overridden with --entrypoint flag. By default, it appends runtime arguments to the defined entrypoint. |
