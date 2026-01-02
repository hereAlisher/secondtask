# First REST API with Spring Boot

A beginner-friendly RESTful API built with Java and Spring Boot that demonstrates basic CRUD operations on a product catalog. This repository is intended for learning how to create and manage REST APIs using Spring Boot and an in-memory H2 database.

## 📦 Features

- Create new products
- Retrieve a single product or list all products
- Update existing products
- Delete products
- H2 in-memory database for easy testing
- Example requests included (curl)

## 🛠 Technologies

- Java 17+
- Spring Boot
- Maven
- H2 Database
- Spring Web

## 📁 Project Structure

```text
src/
└── main/
    └── java/com/springstarter/first_rest_api/
        ├── FirstRestApiApplication.java
        └── product/
            ├── api/
            │   ├── ProductController.java
            │   ├── request/
            │   │   ├── ProductRequest.java
            │   │   └── UpdateProductRequest.java
            │   └── response/
            │       └── ProductResponse.java
            ├── domain/
            │   └── Product.java
            └── repository/
                └── ProductRespository.java
```

## 🚀 Quick Start

### Prerequisites

- Java 17 or newer
- Maven (or use the included Maven wrapper)

### Run locally

Clone the repository and run:

```bash
git clone https://github.com/kingkami0/secondtask.git
cd secondtask
./mvnw spring-boot:run
```

The application starts on http://localhost:8080 by default.

## 🔗 API Endpoints

| Method | Endpoint           | Description             |
|--------|--------------------|-------------------------|
| GET    | /products          | Get all products        |
| GET    | /products/{id}     | Get product by ID       |
| POST   | /products          | Create a new product    |
| PUT    | /products/{id}     | Update existing product |
| DELETE | /products/{id}     | Delete a product        |

### Example curl requests

- Create
```bash
curl -X POST http://localhost:8080/products \
  -H "Content-Type: application/json" \
  -d '{"name":"Example Product","price":19.99,"description":"A sample product."}'
```

- Get all
```bash
curl http://localhost:8080/products
```

- Get by ID
```bash
curl http://localhost:8080/products/1
```

- Update
```bash
curl -X PUT http://localhost:8080/products/1 \
  -H "Content-Type: application/json" \
  -d '{"name":"Updated Name","price":29.99,"description":"Updated description."}'
```

- Delete
```bash
curl -X DELETE http://localhost:8080/products/1
```

## 🗃 H2 Database Console

The app uses an H2 in-memory database. Access the console at:

http://localhost:8080/h2-console

- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (leave blank)

## 🧪 Testing

Use Postman, curl, or any HTTP client to test endpoints. Because the DB is in-memory, data will be reset when the application restarts.

## 📸 Screenshots

Here are also the screenshots : 
![database.png](first-rest-api-java-master/first-rest-api-java-master/screenshots/database.png)
![delete.png](first-rest-api-java-master/first-rest-api-java-master/screenshots/delete.png)
![get.png](first-rest-api-java-master/first-rest-api-java-master/screenshots/get.png)
![get-all.png](first-rest-api-java-master/first-rest-api-java-master/screenshots/get-all.png)
![post.png](first-rest-api-java-master/first-rest-api-java-master/screenshots/post.png)
![put.png](first-rest-api-java-master/first-rest-api-java-master/screenshots/put.png)

## Contributing

Contributions are welcome. If you plan to add functionality or fix bugs:

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes and push
4. Open a pull request describing your changes


