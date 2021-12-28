# Use an official OpenJDK runtime as a parent image
FROM public.ecr.aws/conekta/openjdk:8-alpine

# set shell to bash
# source: https://stackoverflow.com/a/40944512/3128926
RUN apt-get update && apt-get add bash

# Set the working directory to /app
WORKDIR /app

# Copy the fat jar into the container at /app
COPY /target/docker-java-app-example.jar /app

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Run jar file when the container launches
CMD ["java", "-jar", "docker-java-app-example.jar"]