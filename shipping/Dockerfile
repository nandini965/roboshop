# Use the official Maven image to build the app
FROM maven:3.8.4-openjdk-11 AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy the pom.xml to the working directory
COPY pom.xml .

# Run Maven to download dependencies (cache them for later layers)
RUN mvn dependency:go-offline

# Copy the source code into the container
COPY src /app/src

# Build the application using Maven
RUN mvn clean package -DskipTests

# Use a smaller image to run the app
FROM openjdk:11-jre-slim

# Set the working directory for the final image
WORKDIR /app

# Copy the JAR file from the builder stage
COPY --from=builder /app/target/*.jar /app/app.jar
EXPOSE 8080

# Run the application
ENTRYPOINT ["java", "-jar", "/app/app.jar"]
