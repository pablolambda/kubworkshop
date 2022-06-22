FROM registry.access.redhat.com/redhat-openjdk-18/openjdk18-openshift:1.12-1.1655301789
EXPOSE 8080
WORKDIR /src/jars
COPY passwordapi.jar /src/jars
CMD ["java", "-jar", "/src/jars/passwordapi.jar"]
