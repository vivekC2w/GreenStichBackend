# GreenStichBackend

# GreenStitch Authentication API

This project is a Spring Boot-based REST API for user authentication and authorization. It includes endpoints for user login and signup, utilizes JSON Web Tokens (JWT) for security, and stores user data in an H2 database.

## Prerequisites

- Java 11 or higher
- Maven (for building and running the project)

## Getting Started

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/vivekC2w/GreenStichBackend.git
   ```

2. Navigate to the project directory:

   ```bash
   cd greenstitch-auth-api
   ```

3. Build the project using Maven:

   ```bash
   mvn clean install
   ```

4. Run the application:

   ```bash
   java -jar target/greenstitch-auth-api.jar
   ```

The application will start at `http://localhost:8080`.


## Configuration

- Database configuration (H2 by default): You can modify the database settings in `src/main/resources/application.properties`.

- JWT Configuration: JWT secret and expiration settings can be found in the same `application.properties` file.

## API Endpoints

- **POST /api/signup**
  - Create a new user account.
  - Request Body:
    ```json
    {
        "username": "newuser",
        "password": "password123"
    }
    ```
  - Response:
    ```json
    "User registered successfully"
    ```

- **POST /api/login**
  - Authenticate and generate a JWT token.
  - Request Body:
    ```json
    {
        "username": "existinguser",
        "password": "password123"
    }
    ```
  - Response:
    ```json
    {
        "token": "your.jwt.token.here"
    }
    ```

- **GET /api/hello**
  - Access a protected resource.
  - Response:
    ```json
    "Hello from GreenStitch"
    ```
