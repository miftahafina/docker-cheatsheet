# Docker Cheat Sheet

```
docker info
docker version

docker images
docker image ls
docker pull [image-name]:[tag-name]

docker container ls
docker container ls --all (include non running container)
docker container create --name [container-name] [image-name]:[tag-name]
docker container create --name [container-name] -p [host-port]:[container-port] [image-name]:[tag-name]
docker container start [container-name]
docker container stop [container-name]
docker container rm [container-name]

docker image rm [image-name]:[tag-name]
docker image rm [image-id]

Dockerfile
===
FROM [image-name]:[tag-name]
COPY [filename] /app/[filename]
CMD ["cmd1", "cmd2", "/app/[filename]"]
===
docker build --tag [image-name]:[tag-name] .

https://hub.docker.com/repository/create
docker login
docker tag [local-image-name]:[local-tag-name] [repo-image-name]:[repo-tag-name]
docker push [docker-id]/[image-name]:[tag-name]

docker container inspect [container-name]
docker network --help
docker network create [network-name]
docker network ls
docker network connect [network-name] [container-name-1]
docker network connect [network-name] [container-name-2]
docker container inspect [container-name-1]
=> on "Networks" key

docker container create --name [container-name] -p [host-port]:[container-port] -e [ENV_VAR_NAME1]=[env_var_value1] -e [ENV_VAR_NAME2]=[env_var_value2]
```
