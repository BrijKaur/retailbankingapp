FROM servergurus/ubuntu-jdk8

#WildFly Setup 
COPY wildfly-8.2.0 /opt/wildfly

# install retailbank-app-1.0 app on wildfy
COPY retailbank-app-1.0.war /opt/wildfly/standalone/deployments/

RUN java -version

# Expose the required ports
EXPOSE 8081 9990 9090
 
# This will boot WildFly in the standalone mode and bind to all interface -- This is the command which will run will PID=1
CMD ["/opt/wildfly/bin/standalone.sh", "-c", "standalone-full.xml", "-b", "0.0.0.0"]
