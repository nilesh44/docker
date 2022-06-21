# docker
refer this https://docs.docker.com/engine/reference/run/

**Commands to show list of docker images present in local machine**

- docker images

**Remove docker images**
- docker images rm <image-id>

**Show list of container present in docker**

- docker container ls -a
- docker ps
 
 **Stop container**
 
 - docker container stop <container-id>
 - docker container kill <container-id>
**remove all non running container**
 - docker container prune
**Pull docker images from docker repository**

- docker pull <e.g mysql>

**run container**
- docker run 
 e.g run mysql instance on docker container
 docker run -p 13306:3306 --name mysql-docker -e MYSQL_ROOT_PASSWORD=Password -d mysql:latest
 
 Connecting to MySQL Server from within the container
 docker exec -it (name of mysql image)mysql-docker mysql -u (username)root -p
