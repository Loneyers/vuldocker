FROM openjdk:8-jdk-alpine
MAINTAINER Loneyer

VOLUME /tmp
ADD jolokia-xxe.jar /tmp/jolokia-xxe.jar
ENTRYPOINT ["java","-jar","/tmp/jolokia-xxe.jar"]