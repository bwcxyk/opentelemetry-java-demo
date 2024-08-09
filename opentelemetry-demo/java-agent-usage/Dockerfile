FROM amazoncorretto:8-alpine-jre

LABEL maintainer="yaokun@bwcxtech.com"

COPY opentelemetry-javaagent.jar /opt

ENV JAVA_TOOL_OPTIONS=-javaagent:/opt/opentelemetry-javaagent.jar

COPY target/*.jar /home/app.jar
WORKDIR /home

ENTRYPOINT ["/bin/sh", "-c", "java ${JAVA_OPTS} -jar app.jar"]
