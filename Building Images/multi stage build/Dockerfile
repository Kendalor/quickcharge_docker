# First Part: generating the necessary Jars
FROM maven AS builder

WORKDIR ./temp
COPY ./src ./src
COPY ./pom.xml pom.xml
RUN ls
RUN mvn clean install


# Second Part: moving generated Jars in new image, and setting Entrypoint
FROM java 

WORKDIR ./app
RUN ls
COPY --from=builder ./temp/target/myproject-0.0.1-SNAPSHOT.jar ./myproject-0.0.1-SNAPSHOT.jar
RUN ls 
EXPOSE 8080
ENTRYPOINT [ "java", "-jar",  "myproject-0.0.1-SNAPSHOT.jar"]


