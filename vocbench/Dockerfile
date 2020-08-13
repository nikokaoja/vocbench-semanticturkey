FROM tomcat:8.0-alpine

RUN apk update && apk upgrade && apk add --no-cache curl

RUN curl -L https://github.com/niva83/vocbench-semanticturkey/raw/master/vocbench/vocbench.war -o vocbench.war \
    && curl -L https://github.com/niva83/vocbench-semanticturkey/raw/master/vocbench/tomcat-users.xml -o tomcat-users.xml \
    && curl -L https://raw.githubusercontent.com/niva83/vocbench-semanticturkey/master/vocbench/vbconfig.js -o vbconfig.js \
    && cp vocbench.war /usr/local/tomcat/webapps/ \
    && cp tomcat-users.xml /usr/local/tomcat/conf/ \
    && cp vbconfig.js /usr/local/tomcat/webapps/ \
    && rm vocbench.war \
    && rm tomcat-users.xml \
    && rm vbconfig.js

EXPOSE 8080
CMD ["catalina.sh", "run"]