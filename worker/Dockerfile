FROM maven:3.8.4-jdk-11-slim AS builder

LABEL author="Lucas Hauszler"

WORKDIR /app
COPY pom.xml ./

RUN mvn dependency:resolve
COPY . .
RUN mvn package

FROM openjdk:11-jre-slim

WORKDIR /app

COPY --from=builder /app/target/worker-jar-with-dependencies.jar .

CMD [ "java", "-jar", "worker-jar-with-dependencies.jar" ]
