# Job & Company Management API

This is a Spring Boot project that provides RESTful APIs for managing **Companies**, **Jobs**, and **Reviews**. It uses an in-memory H2 database for data persistence, making it easy to run and test locally.

---

## Project Overview

This project allows users to:

- Create, read, update, and delete **Companies**.
- Create, read, update, and delete **Jobs**.
- Add, update, view, and delete **Reviews** for specific companies.

It is designed for learning purposes and can be extended into a full-fledged job portal application.

## Features

- Manage Companies, Jobs, and Reviews  
- CRUD operations for all entities  

---

## Technologies

- Java 17  
- Spring Boot  
- Spring Web  
- Spring Data JPA  
- H2 Database  

---

## Running the Project

1. Clone the repo:

git clone https://github.com/Asad-code79/job-portal-api.git  
cd job-portal-api  

2. Run the application:

mvn spring-boot:run  

3. Access H2 Console: http://localhost:8080/h2-console  
   - JDBC URL: jdbc:h2:mem:test  
   - Username: sa  
   - Password: leave empty  

---

## API Endpoints & Entity Fields

### Companies
Fields:  
- id (Long)  
- name (String)  
- description (String)  

Endpoints:  
- GET /companies  
- GET /companies/{id}  
- POST /companies  
- PUT /companies/{id}  
- DELETE /companies/{id}  

### Jobs
Fields:  
- id (Long)  
- title (String)  
- description (String)  
- minSalary (String)  
- maxSalary (String)  
- location (String)  
- company (Company)  

Endpoints:  
- GET /jobs  
- GET /jobs/{id}  
- POST /jobs  
- PUT /jobs/{id}  
- DELETE /jobs/{id}  

### Reviews
Fields:  
- id (Long)  
- title (String)  
- description (String)  
- rating (double)  
- company (Company)  

Endpoints:  
- GET /companies/{companyId}/reviews  
- GET /companies/{companyId}/reviews/{reviewId}  
- POST /companies/{companyId}/reviews  
- PUT /companies/{companyId}/reviews/{reviewId}  
- DELETE /companies/{companyId}/reviews/{reviewId}  

---

## Configuration

application.properties:  
spring.application.name=Job  
spring.h2.console.enabled=true  
spring.datasource.url=jdbc:h2:mem:test  
spring.jpa.hibernate.ddl-auto=update  

---

## Author

Asad Ameen  
GitHub: https://github.com/Asad-code79
