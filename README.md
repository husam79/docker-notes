# Docker Commands & Notes
Common Docker's commands and notes

## Commands
|Command|Description|
|---|---|
|docker ps|displays all running containers|
|docker run -d -p [host-port]:[container-port] --name [container-name] [img-name]|running a container with a specified [img-name]|
||-d: detach mode|
||-p [host-port]:[container-port] link a host port with a container port|
||--name [container-name]: you can optionally specify a name for this container, to refer to it instead of the container id.|
