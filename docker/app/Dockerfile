FROM openjdk:11 as BUILD-IMAGE
RUN apt update && apt install -y maven
WORKDIR /app
COPY src /app/src
COPY pom.xml /app
RUN mvn install

FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD-IMAGE /app/target/*.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]