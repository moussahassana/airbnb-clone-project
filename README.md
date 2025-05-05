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