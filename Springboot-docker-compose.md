
# For springboot app and docker compose file refer this https://github.com/nilesh44/coffee-customer/blob/main/docker-compose.yml

# Step 1 : pull this repo from git repo 
note: it should have Dockerfile

  it should having docker-compose.yml file
      
# Step 2 : run below command where docker-compose file is present.

docker-compose down && docker-compose build --no-cache && docker-compose up -d

docker-compose down : will remove alrady running services belong to this compose file

docker-compose build --no-cache : create new and fresh docker image 

docker-compose up -d : run newely created fresh image

# Step 3 : verify container is running or not 
docker ps

![image](https://user-images.githubusercontent.com/44174633/180441186-95be0408-afb6-46eb-83c7-f03b9d567c6e.png)

# Step 4 : verify logs
docker logs (container-id)

![image](https://user-images.githubusercontent.com/44174633/180441487-742b2005-b28b-425d-adb8-a884443ee579.png)

Step 5 : test endpoint
![image](https://user-images.githubusercontent.com/44174633/180441624-c8680614-e22e-4089-acfb-cdce6c4fe48d.png)


Note: make sure that this springboot application should be part  of  database network other wise connection won't established

we can verify the network using command

docker inspect (container-d)

![image](https://user-images.githubusercontent.com/44174633/180442860-e99b6951-6b41-4b94-912b-b3d23b38bc50.png)


Note: jdbc url should have name of the mysql container and port (which for internal communication not for external connect)

![image](https://user-images.githubusercontent.com/44174633/180442243-365e9ea5-fe7c-40cf-b35d-07c91cdc4bc4.png)
