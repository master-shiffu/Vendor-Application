# 🛒 Vendor Application

> A full-stack **Vendor Management Web Application** built from scratch to demonstrate core Java, Spring Boot, and Database concepts — designed as a portfolio showcase for prospective employers.
>
> ---
>
> ## 📌 Project Overview
>
> The Vendor Application is a RESTful web application that simulates a real-world vendor management system. It allows users to manage vendors, products, orders, and inventory through a clean API layer backed by a relational database. This project is purpose-built to reinforce and demonstrate backend engineering fundamentals.
>
> ---
>
> ## 🎯 Learning Objectives
>
> - Build and structure a production-ready Spring Boot application from scratch
> - - Design and implement RESTful APIs following best practices
>   - - Apply Object-Relational Mapping (ORM) using JPA and Hibernate
>     - - Secure endpoints using Spring Security with JWT-based authentication
>       - - Write clean, maintainable Java code following SOLID principles
>         - - Model relational data using MySQL and apply normalization concepts
>           - - Manage dependencies and build lifecycle using Maven
>            
>             - ---
>
> ## 🛠️ Tech Stack
>
> | Layer | Technology |
> |---|---|
> | **Language** | Java 17 |
> | **Framework** | Spring Boot 3.x |
> | **API Layer** | Spring MVC (REST APIs) |
> | **Security** | Spring Security + JWT |
> | **ORM** | Hibernate / Spring Data JPA |
> | **Database** | MySQL 8.x |
> | **Build Tool** | Apache Maven |
> | **Version Control** | Git & GitHub |
> | **Testing** | JUnit 5, Mockito |
> | **API Testing** | Postman |
>
> ---
>
> ## 📁 Project Structure
>
> ```
> Vendor-Application/
> ├── src/
> │   ├── main/
> │   │   ├── java/com/vendorapp/
> │   │   │   ├── controller/       # REST Controllers
> │   │   │   ├── service/          # Business Logic Layer
> │   │   │   ├── repository/       # Spring Data JPA Repositories
> │   │   │   ├── model/            # Entity Classes
> │   │   │   ├── dto/              # Data Transfer Objects
> │   │   │   ├── config/           # Security & App Configuration
> │   │   │   └── exception/        # Global Exception Handling
> │   │   └── resources/
> │   │       ├── application.properties
> │   │       └── schema.sql
> │   └── test/                     # Unit & Integration Tests
> ├── .gitignore
> ├── pom.xml
> └── README.md
> ```
>
> ---
>
> ## 🔑 Core Features
>
> - **Vendor Management** — CRUD operations for vendors
> - - **Product Catalog** — Link products to vendors with pricing
>   - - **Order Processing** — Create and track purchase orders
>     - - **User Authentication** — Register, login with JWT token-based auth
>       - - **Role-Based Access Control** — Admin vs. standard user roles
>         - - **Global Exception Handling** — Custom error responses using `@ControllerAdvice`
>           - - **Database Migrations** — Schema management via SQL scripts
>            
>             - ---
>
> ## 🚀 Getting Started
>
> ### Prerequisites
> - Java 17+
> - - MySQL 8+
>   - - Maven 3.8+
>     - - Postman (for API testing)
>      
>       - ### Setup
>      
>       - ```bash
>         # Clone the repository
>         git clone https://github.com/master-shiffu/Vendor-Application.git
>
>         # Navigate to the project directory
>         cd Vendor-Application
>
>         # Configure your MySQL credentials in src/main/resources/application.properties
>         # spring.datasource.url=jdbc:mysql://localhost:3306/vendor_db
>         # spring.datasource.username=your_username
>         # spring.datasource.password=your_password
>
>         # Build and run
>         mvn spring-boot:run
>         ```
>
> ---
>
> ## 📡 API Endpoints (Sample)
>
> | Method | Endpoint | Description |
> |---|---|---|
> | POST | `/api/auth/register` | Register a new user |
> | POST | `/api/auth/login` | Authenticate and get JWT |
> | GET | `/api/vendors` | Get all vendors |
> | POST | `/api/vendors` | Create a new vendor |
> | GET | `/api/vendors/{id}` | Get vendor by ID |
> | PUT | `/api/vendors/{id}` | Update vendor |
> | DELETE | `/api/vendors/{id}` | Delete vendor |
> | GET | `/api/products` | Get all products |
> | POST | `/api/orders` | Place a new order |
>
> ---
>
> ## 🧪 Testing
>
> ```bash
> # Run all tests
> mvn test
> ```
>
> Tests are written using **JUnit 5** and **Mockito** to cover service layer logic and controller endpoints.
>
> ---
>
> ## 📊 Database Schema (ERD Summary)
>
> - **Users** — id, username, password, role
> - - **Vendors** — id, name, email, phone, address
>   - - **Products** — id, name, price, stock_quantity, vendor_id (FK)
>     - - **Orders** — id, user_id (FK), vendor_id (FK), status, created_at
>       - - **Order_Items** — id, order_id (FK), product_id (FK), quantity, unit_price
>        
>         - ---
>
> ## 👨‍💻 Author
>
> **master-shiffu**
> - GitHub: [@master-shiffu](https://github.com/master-shiffu)
>
> - ---
>
> ## 📄 License
>
> This project is open source and available under the [MIT License](LICENSE).
>
> ---
>
> > *Built with dedication to solidify core Java & Spring Boot concepts — one commit at a time.*
