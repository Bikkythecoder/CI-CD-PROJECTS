# Use Tomcat 9 as the base image
FROM tomcat:9.0

# Expose the application port
EXPOSE 8080

# Copy the Maven-generated WAR file into Tomcat
COPY target/*.war /usr/local/tomcat/webapps/
