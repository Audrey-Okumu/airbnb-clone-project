# 🏡Airbnb-clone-project
For Backend

## 📖Overview
This is a backend-focused learning project that recreates the main features of Airbnb's platform.It is designed to help practice skills on backend development, database modelling, authentication, and scalable system designs

### 🏆Project goals
- Implement secure **user registration, login and profile management.**
- Build **property listings** with create , update and retrieval features.
- Add **payment processing** to handle transactions securely.
- Support a **review system** where users can leave ratings and comments.
- Improve efficiency with **database indexing and caching.**

### ⚙️Technology stack

- **Django** - Web framework for backend development
- **Django REST Framework** - REST API support
- **PostgreSQL** - Relational Database
- **GraphQL** - Flexible data queries
- **Celery** - Task queue for background jobs
- **Redis** - Caching and session handling
- **Docker** - Containerization for development and deployment
- **CI/CD Pipelines** - Automated testing and deployments

---

## 👥Team roles

A successful Airbnb Clone project involves collaboration between different specialists, each with a unique responsibility.  

### 🔹 Backend Developer
Responsible for building the application’s **business logic, API endpoints, and database models**. They ensure the system runs smoothly, data flows correctly, and features like authentication, bookings, and payments work securely.

### 🔹 Database Administrator (DBA)
Designs, manages, and optimizes the **database structure**. They implement indexing, backups, and security measures to keep data reliable, consistent, and fast to retrieve.

### 🔹 DevOps Engineer
Ensures smooth **deployment, scaling, and monitoring** of the application. They set up Docker containers, CI/CD pipelines, and cloud infrastructure so the system is reliable and easy to maintain.

### 🔹 QA Engineer (Quality Assurance)
Tests all features to confirm they work as expected. They design test cases, perform manual and automated testing, and report bugs to maintain high-quality standards.

### 🔹 Project Manager 
Coordinates the team by defining tasks, timelines, and goals. They act as the bridge between developers and stakeholders, making sure the project stays on track.

### 🔹 UI/UX Designer
Although this is a backend-focused project, a UI/UX designer may contribute by **designing user-friendly interfaces** and ensuring smooth user flows when the frontend is built.

---

## ⚙️ Technology Stack

The Airbnb Clone project leverages a modern backend stack to ensure scalability, security, and efficiency. Below is an overview of the technologies used and their purpose in the project:

- **Django** – A high-level Python web framework for building the backend and handling business logic.
- **Django REST Framework (DRF)** – Provides tools to build RESTful APIs for user, property, booking, and payment management.
- **PostgreSQL** – A powerful relational database system used for storing and querying project data efficiently.
- **GraphQL** – Allows flexible and efficient data queries, giving clients control over the data they fetch.
- **Celery** – Handles background tasks such as sending notifications, processing payments, or email confirmations.
- **Redis** – Used for caching frequently accessed data and managing asynchronous task queues with Celery.
- **Docker** – Provides containerization for consistent development and deployment environments.
- **CI/CD Pipelines** – Automates testing, integration, and deployment processes to ensure code reliability and faster delivery.

  ---

  ## 🗄️ Database Design

The database for the Airbnb Clone project is designed to manage users, properties, bookings, reviews, and payments efficiently. Below is an overview of the key entities and their relationships.

### Entities and Fields

- **Users**
  - `id`: Unique identifier for each user
  - `name`: Full name of the user
  - `email`: User’s email (used for login and communication)
  - `password_hash`: Encrypted password for authentication
  - `role`: Defines if the user is a guest or a host

- **Properties**
  - `id`: Unique identifier for each property
  - `title`: Name of the property
  - `description`: Details about the property
  - `location`: Address or geographical location
  - `price_per_night`: Cost per night for booking

- **Bookings**
  - `id`: Unique identifier for each booking
  - `user_id`: References the user making the booking
  - `property_id`: References the pro_

- **Reviews**
  - `id`: Unique identifier for each review
  - `user_id`: References the user who wrote the review
  - `property_id`: References the reviewed property
  - `rating`: Numerical rating (e.g., 1–5 stars)
  - `comment`: Text feedback from the user

- **Payments**
  - `id`: Unique identifier for each payment
  - `booking_id`: References the related booking
  - `amount`: Total amount paid
  - `status`: Payment status (e.g., pending, completed, failed)
  - `payment_date`: Date of the payment

### Relationships
- A **User** can own multiple **Properties** (host role).  
- A **User** can make multiple **Bookings**.  
- A **Booking** is linked to one **Property** and one **User**.  
- A **Review** is linked to one **User** and one **Property**.  
- A **Payment** is tied to one **Booking**.  

