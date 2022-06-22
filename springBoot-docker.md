## Create spring boot Docker image , run spring boot application and link with mysql container running in docker as container.


**Add docker file in spring boot application with name "Dockerfile" without any extention**
e.g Dockerfile
```
FROM openjdk:11
EXPOSE 8080
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} register-user(name of spring boot application jar going to be created) .jar
ENTRYPOINT ["java","-jar","/register-user(name of spring boot application jar going to be created).jar"]
```
## Note

**dataSource properties in application.yml**
```
spring:
  jpa:
    hibernate:
      ddl-auto: update
    properties:
      hibernate:
        dialect: org.hibernate.dialect.MySQL8Dialect
  datasource:
    url: jdbc:mysql://mysql-docker(name of mysql docker container):3306/login_mgt_2
    username: ****
    password: *******
    driver-class-name: com.mysql.cj.jdbc.Driver
```

**create jar by running command**
```
./gradlew clean build
```

**create image of spring boot application**
```
docker build --build-arg JAR_FILE=build/libs/*.jar -t register-user(name of spring boot application jar created) .
```

**run docker image and link mysql**
```
docker run -p 8086:8080 --name register-user-cont2 --link mysql-docker(name of mysql image):mysql -d register-user(name of spring boot application image)
```

**check logs of application**
```
docker logs register-user-cont2(name of container)
```
![image](https://user-images.githubusercontent.com/44174633/174969876-18f5a0ab-5167-4c0b-be63-be9b5ee77e33.png)


**Test  application**
![image](https://user-images.githubusercontent.com/44174633/174967352-488d416e-7871-4aef-878a-374cda6418c2.png)



