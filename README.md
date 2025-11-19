## 🌍 Multilingual Travel Guide – Backend (Spring Boot) ##

A RESTful backend service for the Multilingual Travel Guide Application.
This Spring Boot backend handles all data operations including places, users, authentication, reviews, filters, and search APIs.
It connects to MySQL and provides JSON responses to the React frontend.

## ✨ Features ##

📌 Places API (List, search, filter, view details)

🔍 Search by name or location

🏛 Filter by category (Monument, Historical, Scenic, etc.)

👤 User authentication (Register + Login)

📝 Review system (Add review + Get reviews for a place)

🔗 REST API integration

🗃 Database: MySQL

## 🌍 Cross-Origin enabled for frontend communication

🧪 Unit Tests + Controller Tests (JUnit + Mockito)

🧹 DTO + Mapper architecture

🛡 Validations & error handling

📄 Logging using SLF4J

## 🛠 Tech Stack ##

Backend:

Spring Boot

Spring Web

Spring Data JPA

Hibernate

MySQL

JUnit 5

Mockito

Lombok (optional)

## Database: #

MySQL 8+

## 💡 Project Structure ##
src/
 ├── main/
 │   ├── java/com/travelguide/
 │   │       ├── controller/
 │   │       ├── service/
 │   │       ├── repository/
 │   │       ├── dto/
 │   │       ├── model/
 │   │       ├── util/ (mapper)
 │   │       └── TravelGuideBackendApplication.java
 │   └── resources/
 │       ├── application.properties
 │       └── data.sql (optional seed data)
 └── test/
     ├── service tests
     └── controller tests


## 🔗 API Endpoints ##
Places API
Method	Endpoint	Description
GET	/api/places	Get all places + search + filter
GET	/api/places/{id}	Get specific place details
POST	/api/places	Create new place
Users API

Method	Endpoint	Description
POST	/api/users/register	Register new user
POST	/api/users/login	Login user
GET	/api/users/{id}	Get user by ID
Reviews API

Method	Endpoint	Description
GET	/api/reviews/place/{placeId}	Get all reviews for a place
POST	/api/reviews	Add review


## ⚙️ Setup Instructions ##
1. Clone the repository
git clone https://github.com/pratiksha-bawaskar/travel-guide-backend.git

2. Open in Eclipse / IntelliJ
3. Configure application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/travelguide
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true

spring.jpa.open-in-view=false
server.port=8080

## Run the project ##

Run TravelGuideBackendApplication.java

Backend will start at:
👉 http://localhost:8080

## 🗃 Database Setup ##

Create database in MySQL:

CREATE DATABASE travelguide;


Optional seed data:
Add places in /src/main/resources/data.sql.

## 🧪 Running Tests ##
mvn test


Includes:

Service tests

Controller tests

Repository tests

## 🌐 CORS Support ##

CORS enabled for frontend (React on Vite port):

@CrossOrigin(origins = "*")


## 👩‍💻 Author ##

Pratiksha Bawaskar
- Full Stack Developer | Java | Spring Boot | React | MySQL
