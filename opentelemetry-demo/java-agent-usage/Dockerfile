FROM amazoncorretto:8-alpine-jre

LABEL maintainer="yaokun@bwcxtech.com"

COPY opentelemetry-javaagent.jar /opt

COPY target/*.jar /home/app.jar
WORKDIR /home

ENTRYPOINT ["/bin/sh", "-c", "java ${JAVA_OPTS} -jar app.jar"]
