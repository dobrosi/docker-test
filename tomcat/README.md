```
docker build -t my-tomcat .
docker run --name my-tomcat-container my-tomcat
```
```
docker start my-tomcat-container
docker stop my-tomcat-container
```
```
docker exec my-tomcat-container ls -la
docker exec my-tomcat-container date
docker exec -it my-tomcat-container bash
```