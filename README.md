# Airbnb Clone Project (Backend)

A backend-only Airbnb Clone application to manage property listings, user accounts, bookings, reviews, and payments, providing APIs to support client applications.

## Project Goals
- Build a scalable backend API
- Implement secure user authentication and authorization
- Provide a reliable booking and payment system

## Tech Stack
- Django: Web framework for building RESTful APIs
- PostgreSQL: Relational database for data storage
- GraphQL: Efficient API query language for flexible data retrieval
- Docker: Containerization for consistent environments
- GitHub Actions: CI/CD automation for testing and deployment

## Team Roles and Responsibilities

### Backend Developer
Builds APIs, handles business logic, and integrates with the database.

### Database Administrator (DBA)
Designs and optimizes database schema, ensures data integrity, and manages backups.

### DevOps Engineer
Sets up CI/CD pipeline, manages Docker environments, and ensures deployment automation.

### QA Engineer
Creates automated tests, performs manual testing, and ensures backend quality.

### Project Manager
Oversees task planning, progress tracking, and team coordination.

## Database Design

### Users
- user_id (Primary Key)
- name
- email
- password_hash
- role

### Properties
- property_id (Primary Key)
- title
- description
- location
- price_per_night
- user_id (Foreign Key to Users)

### Bookings
- booking_id (Primary Key)
- user_id (Foreign Key to Users)
- property_id (Foreign Key to Properties)
- start_date
- end_date

### Reviews
- review_id (Primary Key)
- user_id (Foreign Key to Users)
- property_id (Foreign Key to Properties)
- rating
- comment

### Payments
- payment_id (Primary Key)
- booking_id (Foreign Key to Bookings)
- amount
- status
- transaction_date

**Relationships:**
- A User can have multiple Properties (One-to-Many)
- A Property can have multiple Bookings (One-to-Many)
- A Booking belongs to one User and one Property (Many-to-One)
- A Review belongs to one User and one Property (Many-to-One)
- A Payment is associated with one Booking (One-to-One)

## Feature Breakdown

### User Management
Create, update, and authenticate user accounts with secure password handling. Essential for securing user data and enabling personalized experiences.

### Property Management
Allows hosts to add, update, or remove properties with details like description, price, and location. Core functionality for listing availability.

### Booking System
Manage property availability and allow users to create and view bookings. Central to the rental business model.

### Reviews and Ratings
Users can leave feedback and ratings for properties they've booked. Builds trust and helps users make informed decisions.

### Payment Processing
Store payment details and statuses to track completed or pending transactions. Critical for monetization and transaction tracking.

## API Security

### Authentication (JWT or Token-Based)
Verifies user identity for accessing secure endpoints. Crucial for protecting user accounts and personal data.

### Authorization
Ensures only authorized users (e.g., property owners) can modify their resources. Prevents unauthorized access to sensitive operations.

### Rate Limiting
Prevents abuse or brute-force attacks by limiting API requests. Protects system resources and maintains service availability.

### Data Validation
Ensures only safe, sanitized input reaches the backend. Prevents injection attacks and data corruption.

### HTTPS/Encryption
Protects sensitive user and payment data during transmission. Essential for maintaining data confidentiality.

## CI/CD Pipeline

### What is CI/CD?
Continuous Integration (CI) automatically tests every code commit, while Continuous Deployment (CD) automates code releases to staging or production environments. This ensures faster and more reliable deployments with early detection of bugs.

### Tools Used
- GitHub Actions: For automated testing and deployments
- Docker: For containerized environments ensuring consistency
- Pytest: For running automated backend tests

### Benefits
- Faster and more reliable deployments
- Early detection of bugs through automated testing
- Consistent and reproducible builds across environments
