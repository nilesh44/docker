##Create spring boot Docker image


**Add docker file in spring boot application with name "Dockerfile" without any extention**
e.g Dockerfile

FROM openjdk:11
EXPOSE 8080
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} register-user.jar
ENTRYPOINT ["java","-jar","/register-user.jar"]


**create jar by running command**
./gradlew clean build

**create image of spring boot application**
docker build --build-arg JAR_FILE=build/libs/*.jar -t register-user .

**run docker image and link mysql**

docker run -p 8086:8080 --name register-user-cont2 --link mysql-docker:mysql -d register-user


##Note

dataSource properties in application.yml

spring:
  jpa:
    hibernate:
      ddl-auto: update
    properties:
      hibernate:
        dialect: org.hibernate.dialect.MySQL8Dialect
  datasource:
    url: jdbc:mysql://mysql-docker(name of docker container):3306/login_mgt_2
    username: ****
    password: *******
    driver-class-name: com.mysql.cj.jdbc.Driver
