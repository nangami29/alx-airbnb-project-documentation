# Airbnb Clone Backend – Features and Functionalities

This document outlines the main features and functionalities supported by the **Airbnb Clone backend**. The goal is to design and document how different parts of the system (users, properties, bookings, payments, etc.) work together.

---

## Overview

The backend system is responsible for handling data storage, user authentication, property management, bookings, and payments. It ensures all operations are secure, efficient, and well-structured for real-world Airbnb-like functionality.

---

## Core Features

### 1. User Management
- User registration and login
- Role-based access (Guest, Host, Admin)
- Profile updates and account management
- Password hashing and secure authentication

### 2. Property Management
- Hosts can list new properties with descriptions, locations, and prices
- Update or delete existing listings
- Upload and manage property images
- Search and filter properties by location, price, and availability

### 3. Booking System
- Users can book available properties
- View booking history and current reservations
- Booking status management (Pending, Confirmed, Canceled)
- Automatic total price calculation based on stay duration

### 4. Payment System
- Supports multiple payment methods (Credit Card, PayPal, Stripe)
- Links each payment to a booking
- Tracks payment history and timestamps

### 5. Reviews and Ratings
- Guests can leave reviews for properties
- Ratings (1–5 stars) with optional comments
- Hosts can view feedback on their listings

### 6. Messaging System
- Allows communication between users (Host ↔ Guest)
- Stores message history with timestamps

---

## Visual Design

A flowchart of all features and their relationships has been created using **Draw.io** and exported as a PNG file.

📄 **File:** `features-and-functionalities/airbnb_backend_features.png`

---

## Repository Structure

