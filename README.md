# Airbnb Clone Project (Backend)

A backend-only Airbnb Clone application to manage property listings, user accounts, bookings, reviews, and payments, providing APIs to support client applications.
Goals
- Build a scalable backend API.
- Implement secure user authentication and authorization.
- Provide a reliable booking and payment system.
Tech Stack: Django, PostgreSQL, GraphQL, Docker, and GitHub Actions for CI/CD.

# Team Roles and Responsibilities
- Backend Developer - 	Builds APIs, handles business logic, and integrates with the database.
- Database Administrator (DBA) -  Designs and optimizes database schema, ensures data integrity, and manages backups.
- DevOps Engineer - Sets up CI/CD pipeline, manages Docker environments, and ensures deployment automation.
- QA Engineer - Creates automated tests, performs manual testing, and ensures backend quality.
- Project Manager - Oversees task planning, progress tracking, and team coordination

# Technology Stack
- Django	Backend - framework for building APIs and handling business logic.
- PostgreSQL -	Relational database to store users, properties, bookings, and payments.
- GraphQL - Efficient API query language for flexible data retrieval.
- Docker - Containerization for consistent development and production environments.
- GitHub Actions - Automates testing, linting, and deployment.

#  Database Design Overview
 - Users: Contains fields such as id, name, email, password_hash, and role. A user can list multiple properties and make multiple bookings.
 - Properties: Includes id, title, description, location, and price_per_night. Each property belongs to a user (the owner) and can have many bookings and reviews.
 - Bookings: Stores id, user_id, property_id, start_date, and end_date. Each booking is linked to one user and one property.
 - Reviews: Contains id, user_id, property_id, rating, and comment. A user can review multiple properties.
 - Payments: Includes id, booking_id, amount, status, and transaction_date. Each payment is tied to a specific booking.

 # Feature Breakdown

User Management
Create, update, and authenticate user accounts with secure password handling.

Property Management
Allows hosts to add, update, or remove properties with details like description, price, and location.

Booking System
Manage property availability and allow users to create and view bookings.

Reviews and Ratings
Users can leave feedback and ratings for properties they’ve booked.

Payment Processing
Store payment details and statuses to track completed or pending transactions.

# API Security

- Authentication (JWT or Token-Based)	Verifies user identity for accessing secure endpoints.
- Authorization	Ensures only authorized users (e.g., property owners) can modify their resources.
- Rate Limiting	Prevents abuse or brute-force attacks.
- Data Validation	Ensures only safe, sanitized input reaches the backend.
- HTTPS/Encryption	Protects sensitive user and payment data during transmission.

# CI/CD Pipeline Overview
What is CI/CD?
- Continuous Integration (CI) tests every commit, and Continuous Deployment (CD) automates code releases to staging or production environments.

Tools Used:

- GitHub Actions: For automated testing and deployments.

- Docker: For containerized environments.

- Pytest: For running automated backend tests.

Benefits:

- Faster and more reliable deployments.

- Early detection of bugs.

- Consistent and reproducible builds.
