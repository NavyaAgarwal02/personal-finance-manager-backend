# Personal Finance Manager Backend

## Introduction

Welcome to the **Personal Finance Manager Backend** project! This project aims to provide a robust and scalable backend service for managing personal finances, including tracking income, expenses, and generating financial reports. Designed with a focus on efficiency and ease of use, this backend service allows users to seamlessly organize their financial data, categorize transactions, and gain insights into their spending habits.

## Key Features

- **Transaction Management:** 
    - Record and manage transactions with details such as amount, type (income or expense), category, date, reference, and description.
- **Category Tracking:** 
    - Categorize transactions into predefined categories like salary, tips, projects, food, movies, bills, medical, fees, and taxes for better organization and analysis.
- **Financial Reporting:** 
    - Generate detailed financial reports to help users understand their spending patterns and make informed financial decisions.
- **Secure and Scalable:** 
    - Built with security best practices to ensure data integrity and privacy. Scalable architecture to handle growing user data efficiently.
- **API-Driven:** 
    - Expose a comprehensive set of APIs for easy integration with frontend applications, mobile apps, and other services.

## Technology Stack 

- **Node.js:** Backend runtime environment for executing JavaScript code.
- **Express.js:** Web framework for building RESTful APIs.
- **MongoDB:** NoSQL database for storing and managing transaction data.
- **Mongoose:** Object Data Modeling (ODM) library for MongoDB and Node.js.
- **JWT Authentication:** Secure user authentication and authorization.
- **Postman:** API documentation and testing.

## Installation

### Prerequisites

- **Node.js** 
- **MongoDB** 

### Steps

- **Clone the Repository**
    - git clone https://github.com/NavyaAgarwal02/personal-finance-manager-backend.git
    - cd personal-finance-manager-backend

- **Install Dependencies**
    - npm install

- **Set Up Environment Variables**
    - Create a .env file in the root directory and add the following:
    ```json
        PORT=8080
        MONGODB_URI=YOUR_MONGODB_URL
        
- **Run the Application**
    - npm start

The backend server should now be running at **http://localhost:8080.**

## Endpoints

### User
- **Register User:**
  - Endpoint: `POST /api/v1/users/register`
  - Description: Register (sign up) new user on app.

- **Login User:**
  - Endpoint: `POST /api/v1/users/login`
  - Description: Login already registered user.

### Transaction
- **Add Transaction:**
  - Endpoint: `POST /api/v1/transactions/add-transaction`
  - Description: Create user's transaction.

- **Update Transaction:**
  - Endpoint: `POST /api/v1/transactions/edit-transaction`
  - Description: Updates transaction profile section in app.

- **Get Transaction:**
  - Endpoint: `POST /api/v1/transactions/get-transaction`
  - Description: Enables users to get transactions.

- **Delete Transaction:**
  - Endpoint: `POST /api/v1/transactions/delete-transaction`
  - Description: Delete an existing transaction.

## Data Models

### User
The `User` data model represents information about all members that uses this app.

- **Fields:**
  - `name`: String (User's name) 
  - `email`: String (User's email address, unique)
  - `password`: String (User's password)  

- **Example:**
  ```json
  {
    "name": "John Doe",
    "email": "john.doe@gmail.com",
    "password": "123456",
  }

### Transaction
The `Transaction` data model represents information about transactions done by all members of a company.

- **Fields:**
  - `amount`: Number (User's amount)
  - `type`: String (income or expense)
  - `category`: String (Transaction category like salary, tip, project, food, movie, bills, medical, fee and tax)
  - `reference`: String (Transaction reference)
  - `description`: String (Transaction details)
  - `date`: Date (Transaction commited)

- **Example:**
  ```json
  {
    "amount": 2500,
    "type": "income",
    "category": "salary",
    "reference": "INV-001",
    "description": "Monthly salary deposit",
    "date": "2024-07-18"
  }

## Usage

1. **Install Dependencies:**
   ```bash
   npm install
