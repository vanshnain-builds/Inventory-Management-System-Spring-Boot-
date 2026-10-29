# Inventory Management System — Spring Boot REST API

OOPJ (CS336B) MSE2 — Question 2.

A REST API built with Java 17, Spring Boot, Spring JDBC (JdbcTemplate), and MySQL. Use Postman to test the endpoints.

## Requirements
- JDK 17 or newer
- MySQL Server
- IntelliJ IDEA (Maven support)
- Postman

## Setup
1. Execute `database.sql` in MySQL Workbench.
2. Open `src/main/resources/application.properties` and replace `YOUR_MYSQL_PASSWORD` with your local MySQL password. Do not commit a real password.
3. Open the folder containing `pom.xml` in IntelliJ IDEA and let Maven import dependencies.
4. Run `InventoryRestApiApplication.java`.
5. The API base URL is `http://localhost:8080`.

You can also configure `DB_URL`, `DB_USERNAME`, and `DB_PASSWORD` as environment variables.

## REST endpoints

| Method | URL | Purpose |
|---|---|---|
| GET | `/api/products` | List all products |
| GET | `/api/products/101` | Find a product by ID |
| POST | `/api/products` | Add a product |
| PUT | `/api/products/101` | Update a product |
| DELETE | `/api/products/104` | Delete a product |
| GET | `/api/products/low-stock` | List products with quantity below 20, highest price first |
| GET | `/api/products/inventory-value` | Calculate total inventory value |

### Example POST body
```json
{
  "productId": 104,
  "productName": "USB Cable",
  "category": "Electronics",
  "quantity": 12,
  "price": 199.00
}
```

In Postman, choose Body → raw → JSON for POST and PUT. Add a test product before using the DELETE example.

## Submission screenshots
Capture the Model, Controller, Postman response, and IntelliJ project structure after running/testing the project. Include three short AI prompts used during development if requested by the submission format.
