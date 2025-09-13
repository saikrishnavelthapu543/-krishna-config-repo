This repository serves as a centralized configuration store for microservices and supporting components in a Spring Boot / Microservices architecture.
It contains multiple .properties files that define service-specific configurations such as API Gateway, Eureka Server, and Employee-related modules.

📂 Repository Structure

employeApiGateway.properties
Configuration settings for the API Gateway service.

employeEureka.properties
Properties for the Eureka discovery server (service registration and discovery).

employee.properties
Main service configuration for the Employee module.

employeeaddress.properties
Configuration for the Employee Address service/module.

🚀 Purpose

Centralize configuration management across multiple services.

Keep environment-specific properties in one place.

Enable easier maintenance, updates, and version control of configuration files.

🛠️ Usage

Clone this repository:

git clone https://github.com/saikrishnavelthapu543/-krishna-config-repo.git


Copy the required .properties file into your service’s resources folder OR configure your Spring Boot application to read from this repo (via Spring Cloud Config Server).

Example (application.yml):

spring:
  config:
    import: optional:configserver:http://localhost:8888


Update values inside the .properties files based on your environment (Dev / Test / Prod).

🧰 Tech Stack

Spring Boot (services using these configs)

Spring Cloud Config (optional, for centralized config server)

Java Properties format (.properties)

📖 Example Use Case

Employee Service reads from employee.properties

Address Service reads from employeeaddress.properties

Eureka Server uses employeEureka.properties

API Gateway loads configuration from employeApiGateway.properties

👨‍💻 Author

Velthapu Sai Krishna

GitHub: saikrishnavelthapu543
