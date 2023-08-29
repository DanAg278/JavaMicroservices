# JavaMicroservices

This project uses Quarkus, the Supersonic Subatomic Java Framework.

For more information about Quarkus, please visit its website: [https://quarkus.io/](https://quarkus.io/).

## Requisites

Before you can build and run this project, ensure you have the following prerequisites installed on your system:

1. **Java 11:** This project requires Java 11.

2. **GraalVM 22.3:** To build native images of your Quarkus applications, GraalVM is required.

3. **Docker 24.0.2 :** To containerize your microservices and run them using Docker Compose, Docker must be installed on your system.

4. **Maven 3.9.4:** You'll need Maven to build the project.
## Building and Running

Follow these steps to build and run the microservices using Docker Compose:

1. **Build Docker Images for Microservices:**

   Open a terminal and navigate to the root directory of your project. Run the following commands to build Docker images for the `rest-book` and `rest-number` microservices:

   ```shell
   cd path/to/your/project
   mvn package -Dquarkus.package.type=native -Dquarkus.native.container-build=true -Dquarkus.container-image.build

2. **Replace Docker Image Names**
   Open vintagestore-docker.compose.yaml file and replace image: value with your Docker Image created in the previous step.

2. **Run Microservices with Docker Compose**
   Open a terminal and navigate to the root directory of your project. Run the following commands to build Docker images for the `rest-book` and `rest-number` microservices:

   ```shell
   cd path/to/your/project
   docker-compose -f vintagestore-docker-compose.yaml up
 
3. **Stop Microservices**
      ```shell
      docker-compose -f vintagestore-docker-compose.yaml down
