FROM eclipse-temurin:21-jdk AS build

# Copy your application's JAR file into the container
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar

# Define the command to run the application when the container starts
ENTRYPOINT ["java","-jar","/app.jar"]
