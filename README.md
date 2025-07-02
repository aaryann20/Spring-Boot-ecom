# 🛒 Ecom Store - Spring Boot E-commerce Platform

![Java](https://img.shields.io/badge/Java-17+-orange.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.0+-brightgreen.svg)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A full-featured, production-ready e-commerce web application built with **Java Spring Boot**. This platform provides a complete online shopping experience with modern UI/UX design inspired by leading e-commerce platforms like Flipkart and Amazon.

## 🌟 Key Features

### 🔐 Authentication & Security
- **User Registration & Login** with Spring Security
- **Role-based Access Control** (Admin/User roles)
- **Password Encryption** using BCrypt
- **Email Verification** and password reset functionality
- **Session Management** and CSRF protection

### 🛍️ Shopping Experience
- **Product Catalog** with categories and detailed product pages
- **Advanced Search & Filtering** functionality
- **Shopping Cart** with real-time updates
- **Wishlist** feature for saving favorite products
- **Order Management** with order history tracking
- **Multiple Payment Options** support

### 👨‍💼 Admin Dashboard
- **Product Management** (Add, Edit, Delete products)
- **Category Management** with hierarchical structure
- **User Management** and role assignment
- **Order Management** and status tracking
- **Inventory Management** with stock alerts
- **Sales Analytics** and reporting

### 🎨 Modern UI/UX
- **Responsive Design** that works on all devices
- **Clean and Intuitive Interface**
- **Fast Loading** with optimized images
- **Modern Bootstrap Components**
- **Custom CSS Animations**

## 🖥️ Screenshots

### Homepage
![Homepage](src/main/resources/static/img/homepage.png)
*Modern homepage with hero banner and featured products*

### Product Listing
![Product Listing](src/main/resources/static/img/products.png)
*Product catalog with filtering and search capabilities*

### Checkout Process
![Checkout](src/main/resources/static/img/checkout.png)
*Streamlined checkout process with billing information*

## 🛠️ Technology Stack

### Backend
- **Java 17+** - Programming language
- **Spring Boot 3.0+** - Application framework
- **Spring Security** - Authentication and authorization
- **Spring Data JPA** - Data persistence layer
- **Hibernate** - ORM framework
- **MySQL** - Relational database
- **JavaMailSender** - Email service
- **Maven** - Dependency management

### Frontend
- **Thymeleaf** - Server-side template engine
- **Bootstrap 5** - CSS framework
- **jQuery** - JavaScript library
- **Custom CSS/JS** - Enhanced styling and functionality

## 🚀 Getting Started

### Prerequisites
- Java 17 or higher
- MySQL 8.0 or higher
- Maven 3.6+
- IDE (IntelliJ IDEA, Eclipse, or VS Code)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ecom-store.git
   cd ecom-store
   ```

2. **Configure Database**
   
   Create a MySQL database:
   ```sql
   CREATE DATABASE ecom_store;
   ```
   
   Update `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/ecom_store
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   ```

3. **Configure Email Service** (Optional)
   ```properties
   spring.mail.host=smtp.gmail.com
   spring.mail.port=587
   spring.mail.username=your_email@gmail.com
   spring.mail.password=your_app_password
   spring.mail.properties.mail.smtp.auth=true
   spring.mail.properties.mail.smtp.starttls.enable=true
   ```

4. **Build and Run**
   ```bash
   ./mvnw clean install
   ./mvnw spring-boot:run
   ```

5. **Access the Application**
   - Open your browser and navigate to `http://localhost:8080`
   - Admin panel: `http://localhost:8080/admin`

## 👥 Default Users

### Admin Account
- **Email:** admin@ecomstore.com
- **Password:** admin123

### Test User Account
- **Email:** user@ecomstore.com
- **Password:** user123

*Note: These are created automatically on first run. You can also register new accounts.*

## 📁 Project Structure

```
src/
├── main/
│   ├── java/com/ecom/
│   │   ├── config/          # Configuration classes
│   │   ├── controller/      # Spring MVC controllers
│   │   ├── entity/          # JPA entities
│   │   ├── repository/      # Data repositories
│   │   ├── service/         # Business logic services
│   │   ├── dto/             # Data Transfer Objects
│   │   └── util/            # Utility classes
│   ├── resources/
│   │   ├── templates/       # Thymeleaf templates
│   │   ├── static/          # CSS, JS, images
│   │   └── application.properties
└── test/                    # Unit and integration tests
```

## 🔧 Configuration

### Database Configuration
The application uses MySQL by default. You can modify the database configuration in `application.properties`:

```properties
# Database Configuration
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
spring.jpa.show-sql=true

# File Upload Configuration
spring.servlet.multipart.max-file-size=10MB
spring.servlet.multipart.max-request-size=10MB
```

### Security Configuration
Spring Security is configured for:
- Form-based authentication
- Role-based authorization
- CSRF protection
- Session management

## 📊 Features in Detail

### Product Management
- **Category-based Organization**
- **Image Upload & Management**
- **Inventory Tracking**
- **Discount & Pricing Management**
- **Product Variants** (size, color, etc.)

### Order Processing
- **Cart Management**
- **Checkout Process**
- **Order Confirmation**
- **Email Notifications**
- **Order Status Tracking**

### User Features
- **Profile Management**
- **Address Book**
- **Order History**
- **Wishlist**
- **Product Reviews & Ratings**

## 🧪 Testing

Run the test suite:
```bash
./mvnw test
```

For integration tests:
```bash
./mvnw verify
```

## 📈 Performance Optimization

- **Database Indexing** for faster queries
- **Image Optimization** for faster loading
- **Caching** for frequently accessed data
- **Lazy Loading** for JPA entities
- **Connection Pooling** for database connections

## 🔒 Security Features

- **SQL Injection Protection** via JPA/Hibernate
- **XSS Protection** through Thymeleaf escaping
- **CSRF Protection** enabled by default
- **Password Encryption** using BCrypt
- **Session Timeout** configuration
- **Input Validation** on all forms

## 🚀 Deployment

### Local Deployment
```bash
./mvnw clean package
java -jar target/ecom-store-1.0.jar
```

### Docker Deployment
```dockerfile
FROM openjdk:17-jdk-slim
COPY target/ecom-store-1.0.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app.jar"]
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 API Documentation

The application provides RESTful APIs for:
- User management
- Product operations
- Order processing
- Cart management

API documentation is available at: `http://localhost:8080/swagger-ui.html`

## 🐛 Known Issues

- Email service requires proper SMTP configuration
- Large image uploads may require server configuration adjustments
- Session timeout may need adjustment based on usage patterns

## 📋 TODO

- [ ] Add payment gateway integration
- [ ] Implement real-time notifications
- [ ] Add product comparison feature
- [ ] Implement advanced analytics dashboard
- [ ] Add multi-language support
- [ ] Implement caching with Redis

## 📞 Support

For support and questions:
- Create an issue on GitHub
- Email: support@ecomstore.com
- Documentation: [Wiki](https://github.com/yourusername/ecom-store/wiki)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Spring Boot community for excellent documentation
- Bootstrap team for the UI framework
- MySQL team for the reliable database
- All contributors who helped improve this project

---

**Made with ❤️ using Spring Boot**

*This project demonstrates modern e-commerce development practices with Spring Boot, focusing on security, scalability, and user experience.*
