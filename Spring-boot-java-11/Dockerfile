FROM alpine/git as repo

MAINTAINER sarat.e99@gmail.com Sarat Chandra E

#git
WORKDIR /app
RUN git clone https://github.com/spring-projects/spring-petclinic.git

#Maven
FROM maven as build
WORKDIR /app
COPY --from=repo /app/spring-petclinic /app 
RUN mvn install

#jdk
FROM openjdk:11.0.10-jre
WORKDIR /app
COPY --from=build /app/target/spring-petclinic-1.5.1.jar /app 

EXPOSE 8080

CMD ["java", "-jar", "spring-petclinic-1.5.1.jar"] 
