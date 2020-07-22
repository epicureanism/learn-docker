# commands
## docker run [Ref](https://docs.docker.com/engine/reference/commandline/run/)
Run a command in a new container. 
```sh
docker run --name docker-tutorial -dp 888:80 epicureanism/docker101tutorial

# --name
# Specify the local container name

# -d
# detach mode, which means the container will run in background and print container ID

# -p 888:80
# Specify local port (first port number) mapping to port (second port number) in container image.

# epicureanism/docker101tutorial 
# The source of container image 
```

## docker cp
Copy files to container or vice versa.

```sh
docker cp ricky.md docker-tutorial:./
#docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|-
#docker cp [OPTIONS] SRC_PATH|- CONTAINER:DEST_PATH
```

## docker export
Export a container’s filesystem as a tar archive
```sh
docker export -o docker-tutorial.tar docker-tutorial
# -o docker-tutorial.tar docker-tutorial
# Specify the local container name "docker-tutorial" and export this container as "docker-tutorial.tar" file.
```

## docker push
Push the local image to remote

```sh
docker commit docker-tutorial epicureanism/docker101tutorial

docker tag 10639231ba2b epicureanism/docker101tutorial:0.1
# tag the local image ID as a remote image name with version number.

docker push epicureanism/docker101tutorial:0.1
```

