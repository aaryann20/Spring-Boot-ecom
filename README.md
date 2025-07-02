# Spring Boot E-commerce Platform

![Hero Banner](src/main/resources/static/img/ecom.png)

## Overview
This is a full-featured E-commerce web application built with **Java Spring Boot**. The project is designed to provide a robust backend-driven shopping experience, with a modern UI inspired by Flipkart and Amazon.

## Key Features
- **User Authentication & Authorization** (Spring Security)
- **Admin Dashboard** for managing products, categories, and users
- **Product Catalog** with categories, search, and filtering
- **Shopping Cart** and order management
- **Profile Management** for users
- **Order Placement** with billing and payment type selection
- **Email System** for password reset and notifications
- **Modern Responsive UI** (Thymeleaf, Bootstrap, custom CSS)
- **MySQL Database** integration

## Backend Focus
- Built with **Java 17+**, **Spring Boot**, **Spring Data JPA**, and **MySQL**
- Major logic and business rules are handled in the backend
- **Email system** is used for password reset and notifications (JavaMailSender)
- Secure password storage and user management
- RESTful endpoints for all major operations

## Screenshots
### Home Page
![Home Page](src/main/resources/static/img/ecom1.png)

### Product Listing
![Product Listing](src/main/resources/static/img/product_img/iphone%2014.jpg)

### Cart & Checkout
![Cart Page](src/main/resources/static/img/ecom2.jpg)

### Order Placement
![Order Placement](src/main/resources/static/img/ecom3.jpg)

## How to Run
1. Clone the repository
2. Configure your MySQL database in `src/main/resources/application.properties`
3. Run the application with `./mvnw spring-boot:run` or from your IDE
4. Access the app at `http://localhost:8080`

## Credentials
- Default admin/user credentials can be set in the database or via registration

## Technologies Used
- Java, Spring Boot, Spring Security, Spring Data JPA
- Thymeleaf, Bootstrap, custom CSS
- MySQL, Hibernate
- JavaMailSender (for email)

## Folder Structure
- `src/main/java/com/ecom/` - Java source code
- `src/main/resources/templates/` - Thymeleaf HTML templates
- `src/main/resources/static/` - Static assets (CSS, JS, images)

## License
This project is for educational/demo purposes.

---

*Major focus: robust backend, secure authentication, and a real-world e-commerce workflow with a modern UI.* 