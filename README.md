# Simple RESTful API with Spring Boot

This repository contains a simple RESTful API project built with Spring Boot, Java 17, Maven, and PostgreSQL 14, and developed in Visual Studio Code (VSCode).

## Requirements

- Java 17
- Maven
- Spring Boot 3.1.0
- PostgreSQL 14
- Visual Studio Code (with Java Extension Pack installed)

## Getting Started

1. Clone this repository:

```bash
git clone https://github.com/vituu-san/RESTful-API.git
```

2. Navigate to the project directory:

```bash
cd RESTful-API
```

3. Set up PostgreSQL:

- Make sure PostgreSQL 14 is installed and running on your machine.
- Create a new database named `products-api`.
- NOTE: No need to create any table, the API will do it.

4. Configure the database connection:

- Open `src/main/resources/application.properties`.
- Update the database connection properties as needed:

``` bash
spring.datasource.username=your_username
spring.datasource.password=your_password
```

5. Build the project using Maven (open the integrated terminal in VSCode using Ctrl + `) and run:

```bash
mvn clean install
```

6.  In the integrated terminal, run the application:

```bash
mvn spring-boot:run
```

The API will start running at `http://localhost:8080`.

## API Endpoints

You can use Postman to test endpoints.

### GET /api/products

Retrieve all products.

### GET /api/products/{id}

Retrieve a specific product passing ID.

### POST /api/products

Create a new product, passing a name and a value in the body of the request.
Example:
```json
{
  "name": "Washer"
  "value": 579.00
}
```

### PUT /api/products/{id}

Update an existing product passing ID and the new values in the body of the request.
Example:
```json
{
  "name": "PROMO Washer"
  "value": 459.00
}
```

### DELETE /api/products/{id}

Delete a product passing ID.

## Configuration

You can configure the application properties in `src/main/resources/application.properties`.

## Contributing

Contributions are welcome! If you find any issues or want to add new features, please submit a pull request.
