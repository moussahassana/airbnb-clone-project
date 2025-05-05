# 🏡 Airbnb Clone - Backend

## 🚀 Objective
A scalable backend for managing users, property listings, bookings, payments, and reviews—mimicking core Airbnb functionalities.

## 🏆 Key Features
- **User Management**: Registration, authentication, profile handling.
- **Property Listings**: Create, update, retrieve, and delete listings.
- **Booking System**: Book properties with check-in/check-out tracking.
- **Payment Integration**: Secure transaction handling.
- **Review System**: User reviews and ratings for properties.
- **Optimized Performance**: Indexing and caching for speed.

## ⚙️ Tech Stack
- **Backend**: Django, Django REST Framework, GraphQL
- **Database**: PostgreSQL
- **Async Tasks**: Celery + Redis
- **Deployment**: Docker, CI/CD pipelines

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

## 📚 Documentation
- REST API: OpenAPI-compliant Swagger docs
- GraphQL API: Flexible query interface for advanced clients

## 👥 Team Roles

- **Backend Developer**: Implements the server-side logic, builds API endpoints, and ensures robust interaction between the frontend and database.

- **Business Analyst (BA)**: Bridges the gap between business needs and technical teams by translating customer requirements into clear specifications and workflows.

- **Product Owner (PO)**: Owns the product vision and backlog, ensuring that the delivered product meets customer needs and aligns with business strategy.

- **Project Manager (PM)**: Plans, organizes, and monitors the project to ensure timely delivery within budget while coordinating team efforts.

- **UI/UX Designer**: Designs intuitive interfaces and user journeys to maximize usability and enhance overall user experience.

- **Database Administrator (DBA)**: Designs, maintains, and optimizes the database to ensure data integrity, performance, and availability.

- **Software Architect**: Defines the high-level structure of the software, chooses tech stacks, and enforces coding standards for scalability and quality.

- **Software Developer**: Writes, tests, and maintains the codebase, implementing application features and solving technical issues.

- **QA Engineer**: Tests the application to ensure it meets quality standards, performs well in production, and aligns with user requirements.

- **Test Automation Engineer**: Builds and maintains automated test scripts to speed up testing and improve coverage and reliability.

- **DevOps Engineer**: Establishes CI/CD pipelines, manages deployment, monitors system performance, and ensures scalability and reliability of the production environment.