# Spring Boot 3 OAuth2 Security Demo

A Spring Boot 3 application demonstrating modern authentication and authorization using Spring Security, OAuth2, and JWT.

This project shows how to secure REST APIs using industry-standard security approaches.

## Features

- OAuth2 authentication
- JWT token-based security
- Role-based authorization
- Secured REST endpoints
- Spring Security configuration
- User authentication flow
- Exception handling

## Technologies

- Java 17+
- Spring Boot 3
- Spring Security 6
- OAuth2
- JWT
- Maven

## Architecture

```
Client
  |
  |
REST API
  |
Spring Security Filter Chain
  |
Authentication Provider
  |
User Service
  |
Database
```

## Security Flow

1. User authenticates through OAuth2 provider
2. Application validates identity
3. JWT token is generated
4. Client sends JWT with API requests
5. Spring Security validates the token
6. Authorized resources are returned

## Configuration

Example:

```properties
spring.security.oauth2.client.registration.google.client-id=YOUR_CLIENT_ID
spring.security.oauth2.client.registration.google.client-secret=YOUR_SECRET
```

Never commit real credentials.

Use environment variables:

```
CLIENT_ID
CLIENT_SECRET
```

## Running the Application

Requirements:

- Java 17+
- Maven

Run:

```bash
mvn clean install

mvn spring-boot:run
```

## API Example

Request:

```
GET /api/users
Authorization: Bearer <JWT_TOKEN>
```

Response:

```json
{
  "username": "hayk",
  "role": "USER"
}
```

## Future Improvements

- Docker support
- PostgreSQL integration
- Refresh tokens
- Keycloak integration
- Integration tests
- GitHub Actions CI/CD

## License

MIT
