# Docker Commands & Notes
Common Docker's commands and notes

## Commands
|#|Command|Description|
|---|---|---|
|1|docker ps -a|displays all running containers|
|||-a if this parameter is specified, then it will display all container running and stopped|
|2|docker run -d -p [host-port]:[container-port] --name [container-name] [img-name]|running a container with a specified [img-name]|
|||-d: detach mode|
|||-p [host-port]:[container-port] link a host port with a container port|
|||--name [container-name]: you can optionally specify a name for this container, to refer to it instead of the container id.|
|||[img-name]: required, the name of the image like (nginx, ... etc)|
|3|docker start [container-id OR container_name]| Starting a previously stopped container with specified id or name. |
|4|docker stop [container-id OR container_name]| Stopping a running container with specified id or name. |
|3|docker start [container-id OR container_name]| Starting a previously stopped container with specified id or name. |
