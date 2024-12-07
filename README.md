# Spring Boot Exception Handling

This project demonstrates how to handle exceptions in a Spring Boot application. It covers various aspects of exception handling including global exception handling, custom exceptions, and controller-specific exception handling using `@ControllerAdvice`.

## Features

- **Global Exception Handling**: Handles all exceptions across the entire application.
- **Custom Exception Classes**: Demonstrates how to create and use custom exceptions.
- **Exception Response Structure**: A consistent response structure for error messages.
- **Exception Logging**: Logs exception details for debugging purposes.
- **Validation Errors**: Handles validation errors for user input.

## Technologies Used
- Spring Boot 3.x
- Java 17
- Maven
- JUnit 5 for Testing

## Project Structure
- **Controller Layer**: Handles HTTP requests and interacts with services.
- **Service Layer**: Contains business logic.
- **Exception Handling**: Includes `@ControllerAdvice` for global exception handling and custom exception classes.

## How to Run
1. Clone the repository:
    ```bash
    git clone https://github.com/ertugrulgaripardic/spring-boot-exception-handling.git
    ```
2. Navigate to the project directory:
    ```bash
    cd spring-boot-exception-handling
    ```
3. Build and run the application:
    ```bash
    mvn clean install
    mvn spring-boot:run
    
## Example Endpoints
- `/api/example`: Example endpoint with exception handling.
- `/api/validation`: Example endpoint demonstrating validation errors.

## Error Response Format

All error responses will follow a consistent format:
```json
{
  "timestamp": "2024-10-08T12:00:00",
  "status": 400,
  "error": "Bad Request",
  "message": "Validation failed",
  "path": "/api/validation"
}
