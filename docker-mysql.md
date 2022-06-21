docker pull image
 e.g run mysql instance on docker container
 docker run -p 13306:3306 --name mysql-docker -e MYSQL_ROOT_PASSWORD=Password -d mysql:latest
 
 Connecting to MySQL Server from within the container
 docker exec -it (name of mysql image)mysql-docker mysql -u (username)root -p
