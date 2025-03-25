# Spring Boot Microservices Project  

This project demonstrates a **Microservices Architecture** using **Spring Boot**. The architecture includes **Department Service, Employee Service, Service Registry, and API Gateway** to manage inter-service communication, load balancing, and scalability.

---

## 🏗 **Project Overview**  
In this project, we have the following microservices:  

1. **Department Service**: Manages department-related operations (create, update, delete, fetch).  
2. **Employee Service**: Manages employee-related operations and retrieves employees by department.  
3. **Service Registry**: Maintains service instances and enables service discovery.  
4. **API Gateway**: Handles all incoming requests, routes them to the appropriate services, and provides security.  

Each microservice operates **independently**, follows a **domain-driven design**, and communicates via **REST APIs**.

---

## 🏛 **Microservices Architecture**  

### ✅ **Department Service**
- Manages **Department CRUD operations**.
- Uses a **dedicated database**.
- Exposes RESTful APIs.
- Communicates with **Employee Service** to fetch employees for a specific department.

### ✅ **Employee Service**
- Manages **Employee CRUD operations**.
- Uses a **dedicated database**.
- Exposes RESTful APIs.
- Communicates with **Department Service** to retrieve department information.

### ✅ **Service Registry (Eureka Server)**
- A **central registry** that tracks all available services.
- Maintains **load-balanced** connections between services.
- Uses **Netflix Eureka** for service discovery.
- Prevents hard-coded service URLs.

### ✅ **API Gateway**
- Acts as a **single entry point** for all public requests.
- Routes requests to appropriate microservices.
- Adds **security layers**, such as authentication.
- Implements **rate-limiting** and **circuit breaking** for resilience.

---

## 🔧 **Technologies Used**
- **Spring Boot** (REST APIs, Microservices)
- **Spring Cloud Netflix Eureka** (Service Discovery)
- **Spring Cloud Gateway** (API Gateway)
- **Spring Data JPA** (Database Integration)
- **H2 / MySQL** (Database)
- **Lombok** (Boilerplate code reduction)
- **Swagger UI** (API Documentation)
- **Postman** (API Testing)

---

## 🚀 **How to Run the Project**  

### 1️⃣ **Clone the Repository**  
```
git clone <your-repository-link>
cd springboot-microservices
```
2️⃣ Run the Service Registry (Eureka Server)
```
cd service-registry
mvn spring-boot:run
Eureka Server will start at http://localhost:8761
```
3️⃣ Run the Department Service
```
cd department-service
mvn spring-boot:run
API available at http://localhost:8081
```
4️⃣ Run the Employee Service
```
cd employee-service
mvn spring-boot:run
API available at http://localhost:8082
```
5️⃣ Run the API Gateway
```
cd api-gateway
mvn spring-boot:run
Gateway URL: http://localhost:8080
```
📌 API Endpoints
Department Service
GET /departments/{id} – Get department details

POST /departments – Create a department

Employee Service
GET /employees/{id} – Get employee details

GET /employees/department/{departmentId} – Get employees in a department

POST /employees – Create an employee

API Gateway (Routes)
GET /api/departments/{id} → Calls Department Service

GET /api/employees/{id} → Calls Employee Service

🏆 Advantages of Microservices
✅ Scalability – Scale individual services independently
✅ Fault Tolerance – Services can run separately without affecting others
✅ Improved Maintainability – Smaller codebases for each service
✅ Technology Agnostic – Use different technologies for different services

📜 License
This project is free to use and modify.

🔗 Happy Coding! 🚀

---

### **How to Use This?**
- Copy the above **README.md** content.
- Paste it into your project's **README.md** file.
- Replace `<your-repository-link>` with your actual GitHub repository URL.
- Commit and push the changes to GitHub.

Let me know if you need any modifications! 😊🚀
