# Airbnb Clone Project

## Overview
The **Airbnb Clone Project** is a comprehensive full-stack web application that replicates the core functionalities of the Airbnb platform. This project is designed to simulate the development of a robust booking system, enabling learners to explore backend architecture, database design, API development, CI/CD integration, and team collaboration.

## Project Goals
- Build a scalable and secure Airbnb-like booking platform.
- Develop a deep understanding of backend systems and software project architecture.
- Practice collaborative development workflows using GitHub.
- Apply DevOps practices such as continuous integration and deployment.
- Design a relational database that reflects real-world booking requirements.
- Integrate modern tools and frameworks for a unified development experience.

## Tech Stack
- **Backend Framework**: Django
- **Database**: MySQL
- **API**: REST & GraphQL
- **CI/CD**: GitHub Actions, Docker
- **Version Control**: Git, GitHub
- 
## Team Roles

### 1. Backend Developer
Handles server-side development and API creation using Django.

### 2. Database Administrator
Designs and manages the MySQL database and ensures data integrity.

### 3. DevOps Engineer
Sets up CI/CD pipelines using GitHub Actions and Docker for automated deployment.

## Key Features
- User registration and authentication
- Property listings and management
- Booking and reservation system
- Secure API endpoints
- Admin dashboard
- Automated testing and deployment pipelines

##  Technology Stack

Below are the core technologies used in building the Airbnb Clone Project, along with their purposes:

###  Django
A high-level Python web framework used to build the backend of the application. It provides built-in tools for authentication, ORM, and admin interfaces, making it ideal for developing secure and scalable RESTful APIs.

###  MySQL
A relational database management system (RDBMS) used to store and manage structured data such as user profiles, bookings, listings, and reviews. It supports complex queries and relationships.

###  GraphQL
A query language for APIs that allows clients to request exactly the data they need. It offers more flexibility compared to REST and helps reduce over-fetching or under-fetching of data.

###  Docker
A containerization tool used to package the application and its dependencies into portable containers, ensuring consistency across development, testing, and production environments.

###  Git & GitHub
Version control tools used for source code management and collaboration. GitHub also enables project tracking, pull requests, and CI/CD pipeline integration.

###  GitHub Actions
A CI/CD platform that automates testing and deployment workflows. Used to trigger actions like running tests or deploying the app whenever code is pushed to the repository.

###  Markdown
A lightweight markup language used to write project documentation files like `README.md`. It helps present information clearly and professionally on GitHub.

## 🗃️ Database Design

The Airbnb Clone Project uses a relational database to store and manage data. Below are the main entities (tables), their key fields, and how they relate to one another.

###  1. Users
Represents people who use the platform to either host or book properties.

**Key Fields:**
- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `is_host` (Boolean to determine if the user is a host)

###  2. Properties
Represents properties listed by hosts.

**Key Fields:**
- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `title`
- `description`
- `location`
- `price_per_night`

###  3. Bookings
Represents reservations made by users for a property.

**Key Fields:**
- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `check_in_date`
- `check_out_date`
- `total_price`

###  4. Reviews
Represents feedback given by users after staying at a property.

**Key Fields:**
- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `rating` (1–5 stars)
- `comment`

###  5. Payments
Represents payment transactions for bookings.

**Key Fields:**
- `id` (Primary Key)
- `booking_id` (Foreign Key → Bookings)
- `payment_method`
- `payment_status`
- `amount`

---

###  Entity Relationships

- **A user** can list multiple **properties** (`1-to-many`).
- **A property** can receive multiple **bookings** (`1-to-many`).
- **A user** can make multiple **bookings** (`1-to-many`).
- **Each booking** belongs to one **user** and one **property** (`many-to-1`).
- **A property** can have multiple **reviews** from different **users** (`1-to-many`).
- **Each booking** has one **payment** record (`1-to-1`).

This relational model ensures structured data storage and efficient querying for a scalable backend system.

---

## Repository Structure (Planned)





