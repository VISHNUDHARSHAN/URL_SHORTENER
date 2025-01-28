# URL_SHORTENER

## Project Description

This project is a URL Shortener application built with Spring Boot, offering users the ability to generate shortened URLs and monitor their usage through analytics. It features user authentication and authorization using Spring Security and JWT tokens to ensure secure access. Users can create accounts, generate multiple shortened URLs, track click counts, and view detailed analytics for specific time durations.

## Features

### URL Shortening
* Generate a shortened version of any long URL.

### User Authentication & Authorization

* Secure login and registration with Spring Security.
* Token-based authentication and authorization using JWT.

### URL Analytics

* Track the total number of clicks for each shortened URL.
* View detailed analytics for user-created URLs over specified durations.

### User Dashboard

* Manage all shortened URLs associated with the user's account.
* Monitor URL performance in real-time.

## Technologies Used

* Backend: Spring Boot
* Authentication & Security: Spring Security, JWT (JSON Web Tokens)
* Database: MySQL(for storing user and URL data)
* REST APIs: To handle user requests and data exchange
* Testing Tools: Postman for API testing
* Build Tool: Maven

## How to Run the Project

### 1. Clone the Repository

git clone https://github.com/VISHNUDHARSHAN/URL_SHORTENER.git
cd URL_SHORTENER

### 2. Set Up the Database

Configure the database connection in application.properties.

spring.datasource.url=jdbc:mysql://localhost:3306/url_shortener
spring.datasource.username=yourUsername
spring.datasource.password=yourPassword

### 3. Run the Application

Build and start the Spring Boot application:
mvn spring-boot:run

### 4. Test the API

Use tools like Postman to test API endpoints.

## API Endpoints

Here are the main endpoints for the application:

### Authentication Endpoints

#### POST /api/auth/public/register
Register a new user.

#### POST /api/auth/public/login
Authenticate a user and receive a JWT token.

### URL Management Endpoints
#### POST /api/urls/shorten
Create a shortened URL (requires JWT token).

#### GET /api/urls/myurls
Retrieve all URLs created by the authenticated user.

#### GET /api/urls/analytics/{shortUrl}
Fetch analytics for a specific URL, Click Event by specified Date.

#### GET /api/urls/totalClicks
Total clicks of the url by date.

### Redirection Endpoint
#### GET /{shortUrl}
Redirects to the original URL.

## Contact

For any inquiries or support, please contact:

### Email: vishnudharshan2003@gmail.com
### GitHub: VISHNUDHARSHAN
