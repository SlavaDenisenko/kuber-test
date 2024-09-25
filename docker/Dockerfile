FROM openjdk:17-jdk-slim

MAINTAINER Vyacheslav Denisenko <denisenko.ve21@gmail.com>

COPY build/quarkus-app/lib/ /deployments/lib/
COPY build/quarkus-app/*.jar /deployments/
COPY build/quarkus-app/app/ /deployments/app/
COPY build/quarkus-app/quarkus/ /deployments/quarkus/

EXPOSE 8000
ENV JAVA_OPTS="-Dquarkus.http.host=0.0.0.0"

ENTRYPOINT [ "java", "-jar", "/deployments/quarkus-run.jar" ]