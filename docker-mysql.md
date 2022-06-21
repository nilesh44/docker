refer this for latest mysql images https://hub.docker.com/_/mysql/?tab=tags

**pull mysql images from docker repositorty**
- docker pull <imageName:imageTag>

e.g docker pull mysql:8.0.29

**run mysql instance as container**
- docker run -p 13306:3306 --name mysql-docker -e MYSQL_ROOT_PASSWORD=***** -d mysql:8.0.29

**check running status**
- docker ps
- docker container ls
- docker container ls -a

 ![image](https://user-images.githubusercontent.com/44174633/174786919-b13e6474-6c91-4f59-9847-181ecefaa519.png)
 
 **Connecting to MySQL Server from within the container**
 - docker exec -it (name of mysql image)mysql-docker mysql -u (username)root -p
 
 e.g docker exec -it mysql-docker mysql -u root -p (windows cmd)
 
 winpty docker exec -it mysql-docker mysql -u root -p (git bash)
 
 ![image](https://user-images.githubusercontent.com/44174633/174787846-00d478ec-b7f6-4ab5-afd0-b814e36f182b.png)
 
 **connecting through mysqlwork bench**
 ![image](https://user-images.githubusercontent.com/44174633/174788513-31d079db-0137-46c3-be33-a948304dc99f.png)
 
 **Stop container**
 - docker container stop (container-id) (for smooth stop)
 - docker container kill (container-id) (for immediate stop )
 
 **start Again container**
 - docker container start (container-id)
 
 **remove docker container**
 - docker container rm (container-id)
 
 **remove all docker container which are not running**
 - docker container prune
 

 


