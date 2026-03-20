# Project Documentation

## Setup Guide

### Prerequisites
- Node.js (14.x or later)
- npm (6.x or later)
- Android Studio / Xcode (for mobile app development)

### Installation Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/fank02/ecommerce-mobile-app.git
   ```
2. Navigate to the project directory:
   ```bash
   cd ecommerce-mobile-app
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Run the application:
   ```bash
   npm start
   ```

## Architecture Overview

This project follows a Model-View-Controller (MVC) architecture, providing a clear separation of concerns:

- **Model**: Manages the data and business logic (e.g., product data, user management).
- **View**: Represents the user interface of the application (e.g., screens for displaying products, user authentication).
- **Controller**: Acts as an intermediary between Model and View, handling user input and updating the Model.

The architecture utilizes React Native for cross-platform mobile development, ensuring a smooth user experience on both iOS and Android.

## API Documentation

### Base URL
- `https://api.example.com/v1`

### Authentication
- **Login**: `POST /auth/login`
  - **Body**: `{ "username": "user", "password": "pass" }`
  - **Response**: `{ "token": "JWT_TOKEN" }`

### Products
- **Get All Products**: `GET /products`
  - **Response**:
    ```json
    [
      { "id": 1, "name": "Product 1", "price": 100 },
      { "id": 2, "name": "Product 2", "price": 150 }
    ]
    ```

- **Get Product by ID**: `GET /products/{id}`
  - **Response**:
    ```json
    { "id": 1, "name": "Product 1", "price": 100 }
    ```

### User Management
- **Register User**: `POST /users/register`
  - **Body**: `{ "username": "user", "password": "pass" }`
  - **Response**: `{ "message": "User created successfully" }`

### Cart
- **Add to Cart**: `POST /cart/add`
  - **Body**: `{ "productId": 1, "quantity": 2 }`
  - **Response**: `{ "message": "Product added to cart" }`

---

_This documentation is generated automatically and should be kept up-to-date with the project's progress._