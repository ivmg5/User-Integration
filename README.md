# User Integration System

**Backend and Frontend Integration for Psychological Prescription Management**

## Overview

The User Integration System is a comprehensive web-based application designed for managing user data, psychological descriptions, prescriptions, and feedback. It integrates a backend server using Node.js, Express, and PostgreSQL, with a frontend client built using React.js. This project also features AI capabilities using OpenAI's GPT-3.5-turbo to generate psychological prescriptions and supports an interactive chat interface for diagnostic assistance.

## Table of Contents

- [System Overview](#system-overview)
- [Technologies Used](#technologies-used)
- [Installation Instructions](#installation-instructions)
- [Usage Instructions](#usage-instructions)
- [API Documentation](#api-documentation)
- [Database Schema](#database-schema)
- [Future Enhancements](#future-enhancements)
- [Conclusion](#conclusion)
- [References](#references)

## System Overview

The User Integration System consists of two key components:

- **Backend Server**: Built with Node.js and Express.js, it manages data storage, API endpoints, and integrates AI features.
- **Frontend Client**: Developed in React.js to provide a user-friendly interface.

### Architecture

**Backend:**
- Node.js and Express.js for server-side operations.
- PostgreSQL as the database.
- RESTful API endpoints for CRUD operations.
- Integrates OpenAI API for generating psychological prescriptions.
- Uses the Nearbyy API for enhanced contextual retrieval in the chat.

**Frontend:**
- Built using React.js.
- Communicates with the backend via HTTP requests.
- Features user registration, dashboard, and detailed user views.

## Technologies Used

- **Node.js**: JavaScript runtime for server-side development.
- **Express.js**: Framework for building web applications.
- **PostgreSQL**: Relational database.
- **React.js**: Library for user interface development.
- **OpenAI API**: AI-based prescription generation.
- **Nearbyy API**: For semantic context retrieval.
- **Axios**: HTTP client.
- **Cors**: Middleware for Cross-Origin Resource Sharing.
- **Dotenv**: Manage environment variables.

## Installation Instructions

### Prerequisites

- Node.js (v14+)
- npm or yarn
- PostgreSQL database
- OpenAI API Key
- Nearbyy API Key

### Backend Setup

1. **Clone the Repository**
    ```bash
    git clone https://github.com/ivmg5/User-Integration.git
    ```
2. **Navigate to the Backend Directory**
    ```bash
    cd backend
    ```
3. **Install Dependencies**
    ```bash
    npm install
    ```
4. **Configure Environment Variables**

   Create a `.env` file with:
    ```env
    OPENAI_API_KEY=your_openai_api_key
    NEARBYY_API_KEY=your_nearbyy_api_key
    ```
5. **Set Up the Database**

   Configure the database connection in `config/db.js` and ensure PostgreSQL is running with a database named `catedraapi`.

6. **Run the Server**
    ```bash
    node index.js
    ```

### Frontend Setup

1. **Navigate to the Frontend Directory**
    ```bash
    cd frontend
    ```
2. **Install Dependencies**
    ```bash
    npm install
    ```
3. **Run the Frontend Application**
    ```bash
    npm run dev
    ```
4. **Access the Application**

   Open your browser at [http://localhost:5173](http://localhost:5173)

## Usage Instructions

### Running the Application

Ensure both the backend (port 3000) and frontend (port 5173) are running.

### Navigating the Application

- **Dashboard**: Displays registered users and allows user registration.
- **Registering a User**: Click "Register" to add a new user with required information such as name, email, phone, etc.
- **User Details**: View and manage user information, descriptions, prescriptions, and feedback.

### Prescription Generation

- Enter symptoms in the "Description of Patient Symptoms" field.
- Click "Generate Prescription" to create a prescription using OpenAI's API.
- Save the prescription to the user's record.

### Interactive Chat

- Use the chat interface to inquire about psychological diagnoses.
- Responses consider relevant context with the Nearbyy API for enhanced semantic search.

## API Documentation

### User Endpoints
- **GET /users**: Retrieve all users.
- **GET /users/:id**: Retrieve a specific user.
- **POST /users**: Create a new user.
- **PUT /users/:id**: Update user details.
- **DELETE /users/:id**: Delete a user.

### Description Endpoints
- **GET /description/:userId**: Retrieve user descriptions.
- **POST /description/:userId**: Add a new description.
- **PUT /description/:id**: Update a description.
- **DELETE /description/:id**: Delete a description.

### Feedback Endpoints
- **GET /feedback/:userId**: Retrieve user feedback.
- **POST /feedback/:userId**: Add new feedback.
- **PUT /feedback/:id**: Update feedback.
- **DELETE /feedback/:id**: Delete feedback.

### Chat Endpoints
- **POST /chat**: Generate AI response based on prompt.
- **POST /chat/context**: Generate response with context retrieved via semantic search.

## Database Schema

### Users Table
- **id**: Unique identifier (Primary Key)
- **name**: User's name
- **email**: User's email
- **phone_number**: Phone number
- **address**: Address
- **birth_date**: Birth date
- **gender**: Gender

### Description Table
- **id**: Unique identifier (Primary Key)
- **description**: Symptoms description
- **prescription**: AI-generated prescription
- **user_id**: References Users(id)

### Feedback Table
- **id**: Unique identifier (Primary Key)
- **feedback**: Feedback content
- **user_id**: References Users(id)

## Future Enhancements

- **User Authentication**: Implement secure login and role-based access.
- **Data Encryption**: Encrypt sensitive information.
- **Error Handling**: Improve error messages and handling.
- **Scalability**: Optimize for larger datasets.
- **Advanced AI Models**: Use more sophisticated AI models.
- **Multilingual Support**: Add support for multiple languages.

## Conclusion

The User Integration System is a robust tool for managing patient data and leveraging AI in psychological treatment. This README aims to guide you through setup, usage, and further system understanding.

## References

- [OpenAI API Documentation](https://beta.openai.com/docs/)
- [Nearbyy API Documentation](https://docs.nearbyy.com/)
- [Node.js Official Website](https://nodejs.org/)
- [Express.js Documentation](https://expressjs.com/)
- [React.js Documentation](https://reactjs.org/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
