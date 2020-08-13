FROM tomcat:8.0-alpine

ADD vocbench.war /usr/local/tomcat/webapps/
COPY tomcat-users.xml /usr/local/tomcat/conf/
COPY vbconfig.js /usr/local/tomcat/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]