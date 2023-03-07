# Docker Commands & Notes
Common Docker's commands and notes

## docker commands
```
docker ps
```
  - displays all running containers.
  - If the parameter **-a** is provided, then it will display all running and stopped containers.
<br/>

```
docker run -d -p [host-port]:[container-port] --name [container-name] [img-name]:[tag]
```
running a container with a specified [img-name]:[tag]
  - -d: detach mode.
  - -p [host-port]:[container-port] link a host port with a container port
  - --name [container-name]: you can optionally specify a name for this container, to refer to it instead of the container id.
  - [img-name]: required, the name of the image like (nginx, ... etc)
  - [tag]: optional, represents the version number of the image, if omitted it will be considered 'latest'
  
<br/>

```
docker start [container-id OR container_name]
```
Starting a previously stopped container with specified id or name.
  
<br/>

```
docker stop [container-id OR container_name]
```
Stopping a running container with specified id or name.

<br/>

```
docker images
```
Displays all available images

<br/>

```
docker logs [container-id OR container-name] -f
```
Displaying logs of the specified container, if the **-f** parameter is provided it will logs in streaming mode

<br/>

## docker commands
|#|Command|Description|
|---|---|---|
|7|docker exec -it [container-id OR container-name] /bin/bash (OR /bin/sh)| Allows to connect to the specified container as root user |
|||-it: interactive mode|
|8|docker network ls| List all available networks in docker |
|9|docker network create [network-name]| creating a new network named “network-name” |
|10|docker network connect [network-name] [container-name OR container-id] | Assigning a network to an existing container **NOTE:** you can assign a network directly to an container when first run it using the following command: docker run --network [network-name] [image-name]|
|11|docker build -t [new-img-name]:[tag] .| Building a new docker image based on the Dockerfile founded in the currenc directory |

## docker composer commands
|#|Command|Description|
|---|---|---|
|1|docker-compose -f [name-of-yaml-file] up -d|create all services that located in the yaml file in detach mode (it will create a network also)|
|2|docker-compose -f [name-of-yaml-file] down|stop all services that located in the yaml file (including the network also)|

## Notes
- The difference between run and start commands is that: the run command create a new container from an image, whereas the start container runs a previously stopped container.
- Docker images is a set of layers. The lower layer is the operating system layer (normally it is linux alpain because it is lightweight),  and the top most one is the app layer. And there are a number of other layers (service layers).
- All the data in the container will lost, if the container is restarted.
