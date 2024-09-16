# Capstone Project - Backend

This repository contains the backend code for the **Capstone Project**. The backend is built using **Node.js** and **Express.js** and connects to a **MongoDB** database. It serves as the REST API layer for the frontend, handling authentication, data processing, and database interactions.

## Features

- RESTful APIs for user authentication, data management, and more.
- JWT-based authentication for secure access.
- MongoDB as the database to store and retrieve data.
- Validation and error handling for API requests.
  
## Project Structure

capstone-backend/
├── middleware/
│   └── index.js
├── models/
│   ├── booking.js
│   ├── cleaningservicelist.js
│   ├── quote.js
│   ├── rating&review.js
│   ├── user.js
│   └── userdata.js
├── routes/
│   ├── bookingroutes.js
│   ├── cleaningserviceroutes.js
│   ├── pro.js
│   ├── quote.js
│   ├── rating&review.js
│   └── userroutes.js
├── uploads/
├── .env
├── .gitignore
├── db.js
├── package.json
├── server.js

## Technologies Used
Node.js - JavaScript runtime for server-side programming
Express.js - Web framework for building REST APIs
MongoDB - NoSQL database for data storage
JWT - JSON Web Token for authentication
Mongoose - ODM for MongoDB
dotenv - Environment variables management

API Documentation
The backend provides the following API endpoints:

## Authentication
POST /api/auth/register - Register a new user.
POST /api/auth/login - Login and obtain a JWT token.
User Management
GET /api/users - Retrieve all users (Admin only).
GET /api/users/:id - Get user by ID.
PUT /api/users/:id - Update user by ID.
DELETE /api/users/:id - Delete user by ID.

Additional Endpoints
Add other routes that correspond to the features of your backend, such as booking, cleaning checklist, and appointments.

## JWT Authentication
This backend uses JWT (JSON Web Tokens) for authentication. After logging in, users receive a token that must be included in the Authorization header for subsequent API requests:
Authorization: Bearer <token>

## MongoDB Setup
The backend is connected to a MongoDB database. Make sure to replace <Your MongoDB Connection String> in the .env file with your actual MongoDB connection string. If you're using MongoDB Atlas, the string will look something like this:
MONGODB_URL=mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority
 
## Testing with Postman
You can test the API endpoints using Postman or a similar API testing tool. Import the provided Postman collection (postman_collection.json) into Postman and adjust the environment variables accordingly.