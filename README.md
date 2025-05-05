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

## Technology Stack

- **Django**: A high-level Python web framework used to build the backend and handle HTTP requests.
- **Django REST Framework (DRF)**: A powerful toolkit for building Web APIs in Django, used to implement RESTful endpoints.
- **GraphQL**: A query language that enables clients to request only the data they need, used for efficient and flexible data fetching.
- **PostgreSQL**: A reliable and powerful relational database used to store and manage application data.
- **Celery**: An asynchronous task queue used to handle background tasks like sending notifications or processing payments.
- **Redis**: An in-memory data store used for caching and as a message broker for Celery.
- **Docker**: A containerization tool used to package the application and its dependencies for consistent development and deployment.
- **CI/CD Pipelines**: Automates the process of testing, building, and deploying code changes to ensure faster and safer delivery.

## Database Design

### Entities and Key Fields

- **User**
  - `id`: Unique identifier
  - `name`: Full name of the user
  - `email`: User email address
  - `password`: Hashed password
  - `role`: Indicates if the user is a host or guest

- **Property**
  - `id`: Unique identifier
  - `title`: Title of the property listing
  - `description`: Property details
  - `price_per_night`: Cost per night
  - `owner_id`: References the User who owns the property

- **Booking**
  - `id`: Unique identifier
  - `user_id`: References the User who made the booking
  - `property_id`: References the booked Property
  - `check_in`: Start date of the stay
  - `check_out`: End date of the stay

- **Review**
  - `id`: Unique identifier
  - `user_id`: Reviewer (references User)
  - `property_id`: Reviewed property
  - `rating`: Score given by the user
  - `comment`: Optional user feedback

- **Payment**
  - `id`: Unique identifier
  - `booking_id`: References the related Booking
  - `amount`: Payment amount
  - `status`: Payment status (e.g., completed, pending)
  - `timestamp`: Time of transaction

### Relationships

- A **User** can create multiple **Properties** (1-to-many).
- A **User** can make multiple **Bookings** (1-to-many).
- A **Booking** is linked to one **User** and one **Property** (many-to-1).
- A **Property** can have multiple **Reviews**, each by a **User** (1-to-many).
- A **Payment** is made for one **Booking** (1-to-1).


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

## Team Roles

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