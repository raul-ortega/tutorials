# Docker: basic usage

## my avida repository in docker hub
https://hub.docker.com/repository/docker/raulya/avida

## show images

```
docker images
```
## login in docker.io

```
docker login docker.io
```
## logout

```
docker logout
```

## pull image from docker.io

```
docker pull raulya/avida:2.15
```

## customize image

```
nano Dockerfile
```

## build avida image

```
docker build -t raulya/avida:2.15 .
```

## remove image

```
docker rmi user/repository:tag (example: raulya/avida:2.15
```

## push image to docker.io

```
docker push raulya/avida:2.15
```

## run container

with sh shell:

```
docker run -it raulya/avida:2.15 /bin/sh
```

with bash shell:

```
docker run -it raulya/avida:2.15 /bin/bash
```

## show containers

```
docker ps --all
```

## show exited container

```
docker ps -f "status=exited"
```

## stop container

```
docker stop container_id
```

## remove container

```
docker rm contaienr_id
```
