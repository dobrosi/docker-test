```
docker run hello-world
docker run tomcat
```

```
docker image ls
docker container ls
docker container ls -a
docker ps
docker ps -a
```

```
docker container rm ...
docker rm ...

docker image rm
docker rmi
docker rmi -f

docker container prune
docker image prune
```
Jatek Tomcat-tel
```
docker run -P tomcat
(docker start ...)
(docker ps)
(docker logs ...)
(docker stop ...)
docker run --name my-tomcat -p 1234:8080 tomcat
(docker stop my-tomcat)
(docker start  my-tomcat)
(docker logs my-tomcat)
(docker logs -f my-tomcat)
(docker inspect my-tomcat)
docker run --name my-tomcat -p 1234:8080 tomcat
docker run --name my-tomcat -p 1234:8080 tomcat
(docker rm my-tomcat)
docker run --name my-tomcat -p 1234:8080 --rm tomcat
docker run --name my-tomcat -p 1234:8080 --rm -d tomcat
docker exec -it my-tomcat bash

docker volume create webapps
docker run --rm -d \
    --name my-tomcat \ 
    -p 1234:8080 \
    -v webapps:/usr/local/tomcat/webapps \
    tomcat
docker run --rm -d \
    --name my-tomcat \ 
    -p 1234:8080 \
    -v ./webapps:/usr/local/tomcat/webapps \
    tomcat

docker network create my-net
docker run --rm -d \
    --name my-tomcat \ 
    -p 1234:8080 \
    -v ./webapps:/usr/local/tomcat/webapps \
    --net my-net \
    tomcat
docker run --rm -d \
    --name my-postgres \
    -e POSTGRES_PASSWORD=postgres \
    -p 5432:5432 \
    -v pgdata:/var/lib/postgresql/data \
    --net my-net \
    postgres
```
Portainer
```
docker volume create portainer_data

docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:lts
```
Image build:
```
docker build -t my-tomcat .
```
Image-bol container futtatas:
```
docker run my-tomcat
```
Image-bol container futtatas nevadassal:
```
docker run --name my-tomcat my-tomcat
```
Container futtatas
```
docker start my-tomcat
```
Log megnezese:
```
docker logs my-tomcat
```
Docker registry
```
docker pull registry
docker run --name registry -p 5000:5000 registry
```