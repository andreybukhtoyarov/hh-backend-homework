FROM openjdk:15-jdk-alpine

RUN mkdir /app

RUN mkdir /etc/properties

COPY target/backend.jar /app/

COPY src/etc/backend/hibernate.properties /etc/properties

COPY src/etc/backend/service.properties /etc/properties

ENTRYPOINT ["java","-DsettingsDir=/etc/properties","-jar","/app/backend.jar"]
