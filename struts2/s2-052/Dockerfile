FROM tomcat:7

MAINTAINER loneyer

RUN set -ex \
    && rm -rf /usr/local/tomcat/webapps/* \
    && chmod a+x /usr/local/tomcat/bin/*.sh

COPY s2-052.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
