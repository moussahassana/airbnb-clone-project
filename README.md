# 🏡 Airbnb Clone - Backend

## 🚀 Objective
A scalable backend for managing users, property listings, bookings, payments, and reviews—mimicking core Airbnb functionalities.
## Feature Breakdown

- **User Management**: Allows users to register, log in, and manage their profiles. This feature ensures secure access and personalized user experiences for both guests and hosts.

- **Property Management**: Hosts can create, update, and delete property listings. It enables detailed property information to be displayed for potential guests to view and book.

- **Booking System**: Users can reserve properties for specific dates, including check-in and check-out tracking. This system manages availability and ensures no double bookings.

- **Payment Integration**: Handles secure payments for bookings and records transaction details. It ensures a smooth financial workflow between guests and hosts.

- **Review System**: Users can leave reviews and ratings for properties after their stay. This builds trust and improves decision-making for future guests.

- **Performance Optimization**: Implements database indexing and caching techniques. These enhancements improve response times and reduce server load, ensuring a better user experience.

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

## API Security

To ensure safe and reliable interactions with the system, the following security measures are implemented:

- **Authentication**: Only registered users can access protected endpoints through token-based authentication (e.g., JWT). This protects user accounts and ensures only legitimate users perform actions.

- **Authorization**: Role-based access control (RBAC) is enforced to ensure users can only access data and perform actions appropriate to their roles (e.g., guest vs host). This prevents unauthorized access to sensitive resources.

- **Rate Limiting**: Limits the number of API requests allowed per user/IP within a time window to prevent abuse and denial-of-service (DoS) attacks. It protects system stability and fairness.

Security is critical to protect user data (e.g., personal info, passwords), ensure safe financial transactions (e.g., booking payments), and maintain trust and integrity in the platform.

## CI/CD Pipeline

CI/CD (Continuous Integration and Continuous Deployment) pipelines automate the process of testing, building, and deploying code changes. They ensure that every code update is validated through automated tests and safely deployed to production without manual intervention.

This approach improves development speed, reduces errors, and ensures a consistent delivery workflow. It allows developers to detect bugs early, maintain high code quality, and deploy updates reliably.

**Tools used**:  
- **GitHub Actions**: Automates testing and deployment workflows.
- **Docker**: Ensures consistent environments across development and production.
- **CI/CD scripts**: Custom scripts for building, testing, and deploying the application.

These tools collectively help streamline the release process and ensure smooth updates to the project.


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