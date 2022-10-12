### command to create volume:
~~~
sudo docker volume create --name tomcat-volume
~~~
![image](https://user-images.githubusercontent.com/44174633/195302368-396e6f6d-55b2-4cf1-9bb0-aaee0e9d4288.png)

### get all volume :
~~~
sudo docker volume ls
~~~
![image](https://user-images.githubusercontent.com/44174633/195302740-f0d43cce-b5c8-4a9f-81f7-18246283a088.png)

### remove volume :
~~~
sudo docker volume tomcat-volume
~~~
![image](https://user-images.githubusercontent.com/44174633/195303057-2f2ab5ac-aac6-4b77-8e72-8c3a411095d8.png)

### remove volume that are not in use
~~~
sudo docker volume prune
~~~
