FROM tomcat
COPY tomcat-users.xml /usr/local/tomcat/conf/
COPY manager.xml /usr/local/tomcat/conf/Catalina/localhost/
COPY context.xml /usr/local/tomcat/webapps/host-manager/META-INF/
RUN wget https://excellmedia.dl.sourceforge.net/project/pebble/pebble/2.6.4/pebble-2.6.4.zip  -P /tmp \
  && unzip /tmp/pebble-2.6.4.zip -d /opt \
  && cp /opt/pebble-2.6.4/pebble-2.6.4.war /usr/local/tomcat/webapps \
  && rm /tmp/pebble-2.6.4.zip

EXPOSE 8080
CMD ["catalina.sh", "run"]