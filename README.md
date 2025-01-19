# Spring Boot Exception Handling

This project serves as a comprehensive guide to implementing exception handling in a Spring Boot application, offering a structured approach to managing errors and providing meaningful feedback to users. Exception handling is a critical part of any robust application, ensuring that unexpected errors are gracefully managed without exposing sensitive system details. This project explores several core concepts, including global exception handling, creating and using custom exceptions, and managing controller-specific exceptions through the powerful @ControllerAdvice annotation.

Key Features
Global Exception Handling: This feature allows you to centralize the handling of all exceptions that occur throughout the application. By leveraging the @RestControllerAdvice annotation, exceptions are captured at a single point, ensuring consistent and maintainable error management.

Custom Exception Classes: Demonstrates how to design and utilize custom exception classes tailored to specific application needs. These classes improve clarity and allow for more descriptive error messages that align with business logic.

Standardized Exception Response Structure: Provides a uniform structure for error responses returned to the client. This structure includes essential details such as error codes, timestamps, messages, and additional metadata, improving the debugging experience and client interaction.

Exception Logging: Logs detailed exception information, including stack traces, to assist developers in identifying and resolving issues effectively. By integrating logging frameworks like SLF4J or Logback, the project ensures that all exceptions are traceable in production environments.

Validation Error Handling: Implements mechanisms to capture and handle validation errors resulting from incorrect or incomplete user inputs. It demonstrates how to extract validation messages and return clear, actionable feedback to users.

This project not only enhances the resilience of the application but also lays a foundation for building applications that prioritize user experience and maintainability. It is an essential resource for understanding the best practices of exception handling in a modern Spring Boot environment.

## Technologies Use
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
