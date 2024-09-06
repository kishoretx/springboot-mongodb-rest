# Stage 1: Build the application
FROM openjdk:17-jdk-slim

# Set the working directory
WORKDIR /app

# Copy the Maven build files
COPY pom.xml .
COPY src ./src

# Build the application
RUN mvn clean package -DskipTests

# Stage 2: Create the runtime image
FROM openjdk:17-jdk-slim

# Set the working directory
WORKDIR /app

# Copy the jar file from the build stage
COPY target/springboot-mongodb-rest-0.1.jar /app/springboot-mongodb-rest.jar

# Expose the port the app runs on
EXPOSE 8080

# Command to run the application
CMD ["java", "-jar", "springboot-mongodb-rest.jar"]
