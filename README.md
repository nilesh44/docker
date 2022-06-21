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
 
 **check running status**
 - docker stats
 ![image](https://user-images.githubusercontent.com/44174633/174795099-f443ec39-5aa7-42f0-b929-01784041892f.png)

 **check ProcessId of container**
 - docker top (container-id)
 ![image](https://user-images.githubusercontent.com/44174633/174795564-5d308901-f623-418b-8c02-3613349235d6.png)
 
 **docker system**
 --docker system df
 ![image](https://user-images.githubusercontent.com/44174633/174796101-4538bc8a-ce98-4d27-854e-235a5b98937a.png)

 Add docker file 
 ./gradlew clean build
 docker build --build-arg JAR_FILE=build/libs/*.jar -t register-user .

