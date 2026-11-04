# Library API

A Spring Boot REST API for managing books in a library.

## Technology

- Java 21
- Spring Boot
- Spring Data JPA
- MySQL
- Maven

## Database setup

Create a MySQL database named `library_db`, then configure the connection details in:

`src/main/resources/application.properties`

The application uses Hibernate's `update` mode, so existing tables are preserved while entity changes are applied.

## Run the application

On Windows:

```cmd
mvnw.cmd spring-boot:run
```

The API starts at `http://localhost:8080`.

## API endpoints

Base URL: `/api/books`

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/books` | Create a book |
| GET | `/api/books` | Get all books |
| GET | `/api/books/{id}` | Get a book by ID |
| PUT | `/api/books/{id}` | Update a book |
| DELETE | `/api/books/{id}` | Delete a book |

Example request body:

```json
{
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "isbn": "9780132350884",
  "price": 45.00
}
```
