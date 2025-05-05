# 🏡 Airbnb Clone - Backend

## 🚀 Objective
A scalable backend system for managing users, property listings, bookings, payments, and reviews—mimicking the core functionalities of Airbnb.

---

## 🧩 Feature Breakdown

- **User Management**: Allows users to register, log in, and manage their profiles. Ensures secure access and personalized user experiences for both guests and hosts.

- **Property Management**: Enables hosts to create, update, and delete property listings. Guests can view and filter available properties before booking.

- **Booking System**: Allows users to reserve properties with defined check-in and check-out dates. Prevents double-booking and manages availability.

- **Payment Integration**: Handles secure transactions between guests and hosts. Records and tracks payment statuses.

- **Review System**: Users can leave reviews and ratings for properties. Builds trust within the platform through user feedback.

- **Performance Optimization**: Implements indexing and caching to improve database performance and response time.

---

## 🛠️ Technology Stack

- **Django**: A high-level Python web framework used to build the backend and handle HTTP requests.
- **Django REST Framework**: Toolkit for building RESTful APIs in Django.
- **GraphQL**: A flexible query language used for efficient data retrieval.
- **PostgreSQL**: Relational database used to store and manage structured data.
- **Celery**: Manages background tasks like email notifications and payment processing.
- **Redis**: In-memory data store used for caching and message brokering.
- **Docker**: Ensures consistent development and production environments through containerization.
- **CI/CD Pipelines**: Automates testing, building, and deployment of the application.

---

## 🗃️ Database Design

### Entities and Key Fields

- **User**
  - `id`, `name`, `email`, `password`, `role`

- **Property**
  - `id`, `title`, `description`, `price_per_night`, `owner_id`

- **Booking**
  - `id`, `user_id`, `property_id`, `check_in`, `check_out`

- **Review**
  - `id`, `user_id`, `property_id`, `rating`, `comment`

- **Payment**
  - `id`, `booking_id`, `amount`, `status`, `timestamp`

### Entity Relationships

- A **User** can create multiple **Properties**.
- A **User** can make multiple **Bookings**.
- A **Booking** is linked to one **User** and one **Property**.
- A **Property** can have many **Reviews** from different **Users**.
- A **Payment** is associated with a single **Booking**.

---

## 🔐 API Security

- **Authentication**: Token-based (e.g., JWT) authentication to secure endpoints and validate user identity.
- **Authorization**: Role-based access control (RBAC) restricts users to only the actions permitted for their role.
- **Rate Limiting**: Prevents abuse and DoS attacks by limiting the number of requests per user or IP.

Security measures protect sensitive data, secure payments, and maintain trust across the platform.

---

## ⚙️ CI/CD Pipeline

CI/CD (Continuous Integration and Continuous Deployment) pipelines automate testing, building, and deploying code changes. They enable developers to detect bugs early, maintain code quality, and deploy reliably with minimal downtime.

**Tools Used**:
- **GitHub Actions**: Automates testing and deployment workflows.
- **Docker**: Provides consistent environments across stages.
- **Custom CI/CD Scripts**: Handle build, test, and deployment processes.

---

## 📌 API Endpoints Overview

### 👤 Users
- `GET /users/`
- `POST /users/`
- `GET /users/{id}/`
- `PUT /users/{id}/`
- `DELETE /users/{id}/`

### 🏘️ Properties
- `GET /properties/`
- `POST /properties/`
- `GET /properties/{id}/`
- `PUT /properties/{id}/`
- `DELETE /properties/{id}/`

### 📆 Bookings
- `GET /bookings/`
- `POST /bookings/`
- `GET /bookings/{id}/`
- `PUT /bookings/{id}/`
- `DELETE /bookings/{id}/`

### 💳 Payments
- `POST /payments/`

### ⭐ Reviews
- `GET /reviews/`
- `POST /reviews/`
- `GET /reviews/{id}/`
- `PUT /reviews/{id}/`
- `DELETE /reviews/{id}/`

---

## 📚 Documentation

- **REST API**: Available through OpenAPI-compliant Swagger documentation.
- **GraphQL API**: Flexible querying interface for clients needing customized data responses.

---

## 👥 Team Roles

- **Backend Developer**: Builds backend logic and APIs for interacting with users, properties, and bookings.
- **Business Analyst (BA)**: Translates customer needs into technical requirements and workflows.
- **Product Owner (PO)**: Defines product vision and priorities to align with user and business needs.
- **Project Manager (PM)**: Oversees planning, coordination, and on-time delivery of the project.
- **UI/UX Designer**: Designs user flows and interfaces for an intuitive and engaging experience.
- **Database Administrator (DBA)**: Manages the database structure, performance, and optimization.
- **Software Architect**: Designs the system architecture and chooses technologies to ensure scalability and maintainability.
- **Software Developer**: Writes and maintains application code to implement core functionality.
- **QA Engineer**: Tests application features to ensure functionality, performance, and reliability.
- **Test Automation Engineer**: Develops automated test scripts to speed up and improve testing accuracy.
- **DevOps Engineer**: Manages infrastructure, CI/CD pipelines, and deployment to production environments.