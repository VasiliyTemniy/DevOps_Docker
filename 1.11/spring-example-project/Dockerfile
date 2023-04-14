FROM openjdk:8u342-slim-bullseye

WORKDIR /usr/src/app

COPY . .

RUN ./mvnw package

CMD java -jar ./target/docker-example-1.1.3.jar