# Airbnb Clone Backend — Requirements Specification
1. Overview

- This document outlines the technical and functional requirements for the main backend features of the Airbnb Clone project.
- The backend is designed to handle users, properties, bookings, and payments securely and efficiently.

2. Key Backend Features
2.1 User Authentication

Description:
Handles user registration, login, and profile access for guests, hosts, and admins.

### Requirements:

- Users can register with first name, last name, email, and password.

- Passwords are encrypted before being stored.

- Login provides a token for session management.

#### API Endpoints:

Method	Endpoint	Description
POST	/api/v1/register	Register a new user
POST	/api/v1/login	Log in a user
GET	/api/v1/profile	Get user profile info

### Validation Rules:

- Unique and valid email required.

- Password must be at least 8 characters.

- Role must be one of: guest, host, admin.

### 2.2 Property Management

- Description:
Allows hosts to create, update, and delete property listings, while guests can browse or view details.

#### Requirements:

- Hosts can add and update their property information.

- Guests can search for available properties.

- Properties include details like name, location, description, and price per night.

### API Endpoints:

Method	Endpoint	Description
POST	/api/v1/properties	Add a new property
GET	/api/v1/properties	View all properties
GET	/api/v1/properties/:id	View specific property
PUT	/api/v1/properties/:id	Update property
DELETE	/api/v1/properties/:id	Delete property

### Validation Rules:

- Price must be greater than zero.

- Only the host who created the property can edit or delete it.

#### 2.3 Booking System

Description:
Manages how users book properties, check availability, and confirm reservations.

### Requirements:

- Users can select dates and make bookings.

- The system calculates the total price automatically.

- Booking status can be pending, confirmed, or canceled.

### API Endpoints:

Method	Endpoint	Description
POST	/api/v1/bookings	Create a booking
GET	/api/v1/bookings/:id	View a booking
PUT	/api/v1/bookings/:id/cancel	Cancel a booking

### Validation Rules:

- End date must be after start date.

- No double-booking allowed.

- Property must exist and be available.

## 3. Non-Functional Requirements

- All API endpoints (except login/register) require authentication.

- Responses should return within 1 second.

- The system must ensure data accuracy and prevent duplicate records.

- Documentation will be provided using Swagger or Postman.