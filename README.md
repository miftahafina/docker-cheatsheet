# Docker Cheat Sheet

## Basic
```
docker info
docker version
```

## Images
```
docker images
docker image ls
docker pull [image-name]:[tag-name]
docker image inspect [image-name]:[tag-name]
docker image rm [image-name]:[tag-name]
docker image rm [image-id]
```

## Container
```
docker container ls
docker container ls --all (include non running container)
docker container create --name [container-name] [image-name]:[tag-name]
docker container create --name [container-name] -p [host-port]:[container-port] [image-name]:[tag-name]
docker container start [container-name]
docker container stop [container-name]
docker container rm [container-name]
```

## Dockerfile
```
File name: Dockerfile
===
FROM [image-name]:[tag-name]
COPY [filename] /[dir-name]/[filename]
CMD ["cmd1", "cmd2", "/[dir-name]/[filename]"]
===
docker build --tag [image-name]:[tag-name] .
```

## Push Image
```
https://hub.docker.com/repository/create
docker login
docker tag [local-image-name]:[local-tag-name] [repo-image-name]:[repo-tag-name]
docker push [docker-id]/[image-name]:[tag-name]
```

## Network Container
```
docker container inspect [container-name]
docker network --help
docker network create [network-name]
docker network ls
docker network connect [network-name] [container-name-1]
docker network connect [network-name] [container-name-2]
docker container inspect [container-name-1]
=> on "Networks" key
```

## Environment Variable
```
docker container create --name [container-name] -p [host-port]:[container-port] -e [ENV_VAR_NAME1]=[env_var_value1] -e [ENV_VAR_NAME2]=[env_var_value2]
```
