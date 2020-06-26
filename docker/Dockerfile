# Create an amapj image out of source/build files delivered by amapj.fr

FROM tomcat:7
LABEL maintainer="jean.pommier@pi-geosolutions.fr"

RUN mkdir -p /opt/amapj/webapp /opt/amapj/amapj-db /opt/amapj/data/logs /opt/amapj/data/backups

COPY dist/amapj-war /opt/amapj/webapp/
COPY dist/amapj-db /opt/amapj/amapj-db/
COPY docker/amapj.xml /usr/local/tomcat/conf/Catalina/localhost/

EXPOSE 8080

VOLUME ["/opt/amapj/data/backups", "/opt/amapj/data/logs", "/opt/amapj/amapj-db"]
