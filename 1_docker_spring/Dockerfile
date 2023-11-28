#FROM adoptopenjdk/openjdk11:alpine-jre

#WORKDIR /opt/app

#ARG JAR_FILE=target/spring-boot-web.jar

#COPY ${JAR_FILE} app.jar

#ENTRYPOINT ["java","-jar","app.jar"]


FROM eclipse-temurin:11-jdk-jammy as builder

WORKDIR /opt/app

COPY .mvn/ .mvn

COPY mvnw pom.xml ./

RUN ./mvnw dependency:go-offline

COPY ./src ./src

RUN ./mvnw clean install
 


FROM eclipse-temurin:11-jre-jammy

WORKDIR /opt/app

EXPOSE 8080

ARG JAR_FILE=spring-boot-web.jar

COPY --from=builder /opt/app/target/${JAR_FILE} /opt/app/${JAR_FILE}

ENTRYPOINT ["java", "-jar", "/opt/app/spring-boot-web.jar" ]
