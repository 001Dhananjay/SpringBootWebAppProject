Spring Boot Thymeleaf CRUD Web Application

This repository contains a Spring Boot CRUD web application that demonstrates Pagination and Sorting features, implemented with Spring Boot, Thymeleaf, Spring MVC, Spring Data JPA, Hibernate, and MySQL.


Features

1.CRUD Operations:

  # Perform Create, Read, Update, and Delete operations on employee records.

2.Pagination:

  # Navigate through data in smaller, manageable pages.

3.Sorting:

  # Dynamically sort records by specific fields.

Prerequisites

1.Java Development Kit (JDK): Version 8 or higher.

2.Maven: For dependency management.

3.MySQL Database: Ensure a running instance of MySQL.

4.IDE: IntelliJ IDEA, Eclipse, or any preferred IDE.

Setup Instructions

1. Clone the repository:

2. Configure MySQL Database:

# DATASOURCE (DataSourceAutoConfiguration & DataSourceProperties)
spring.datasource.url=jdbc:mysql://localhost:3306/hibernate_mapping?useSSL=false&serverTimezone=UTC&useLegacyDatetimeCode=false
spring.datasource.username=root
spring.datasource.password=Ashlok@123

# Hibernate
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto=update

logging.level.org.hibernate.SQL=DEBUG
logging.level.org.hibernate.type=TRACE

3. Build the project:
    mvn clean install

4. Run the application:
    mvn spring-boot:run

5. Access the application:
   # Open a browser and navigate to http://localhost:8080

Application Structure

1. Controller Layer:

  # Handles HTTP requests and maps them to appropriate service methods.

2. Service Layer:

  # Contains business logic and communicates with the repository layer.

3. Repository Layer:

  # Performs database operations using Spring Data JPA.

4. View Layer:

  # HTML templates rendered by Thymeleaf.

Pagination and Sorting

 # Pagination:

   - Allows navigating through large datasets page by page.

   - Configured using Spring Data JPA's Pageable interface.

 # Sorting:

   - Supports dynamic sorting by passing sort parameters in requests.

Dependencies

 - Spring Boot Starter Web

 - Spring Boot Starter Thymeleaf

 - Spring Boot Starter Data JPA

 - MySQL Connector