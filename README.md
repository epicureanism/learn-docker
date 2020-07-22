# commands
```sh
docker run --name docker-tutorial -dp 888:80 epicureanism/docker101tutorial
```
> docker run

Run a command in a new container. [Ref](https://docs.docker.com/engine/reference/commandline/run/)

> --name

Specify the local container name

> -d

detach mode, which means the container will run in background and print container ID

>-p 888:80

Specify local port (first port number) mapping to port (second port number) in container image.

> epicureanism/docker101tutorial 

The source of container image 
