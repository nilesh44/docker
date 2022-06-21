# docker
refer this https://docs.docker.com/engine/reference/run/

**Commands to show list of docker images present in local machine**

- docker images

**Show list of container present in docker**

- docker container ls -a

**Pull docker images from docker repository**

- docker pull <e.g mysql>

**run container**
- docker run 
 e.g run mysql instance on docker container
 docker run -p 13306:3306 --name mysql-docker -e MYSQL_ROOT_PASSWORD=Password -d mysql:latest
