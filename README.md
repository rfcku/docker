# Docker 101
`docker ${ACTION} ${--OPTIONS} ${IMAGE}`
## `run`
```
docker run hello-world
```
**run**         =   `${ACTION}`
**hello-world** =   `${IMAGE}`
## `ports`
```
docker run -p 80:80 nginx
-   Multiple ports: 
docker run -p 80:80 -p 80:33070 nginx
```
**-p** = `${--OPTIONS.PORT}`
## `detached`
```
$ docker run -p 80:80 -d nginx
```
**-d** = `${OPTIONS.DETACHED}`
## `ps`
```
$ docker ps
$ docker ps | grep nginx
```
**ps** = `${ACTION}`
## `logs`
```
$ docker logs ${CONTAINER_ID}
```
## `exec`
```
$ docker exec -it ${CONTAINER_ID} ${ACTION}
```
**-it** = `${INTERACTIVE}`
## `build`
```
$ docker build -t ${IMAGE.TAG} ${DOCKERFILE.LOCATION}
```