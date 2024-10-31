# **User Integration System**
> *A comprehensive web application for managing patient data and AI-assisted psychological prescription generation.*

## **Introduction**
The User Integration System is developed to streamline patient data management in psychology, integrating AI to assist professionals in generating psychological prescriptions and performing diagnostic assessments. This tool allows psychologists to manage patient data, including symptoms, feedback, and prescriptions, all within an interactive, easy-to-use application.

## **Project Description**
- **Main functionality:** Facilitates the management of patient records, AI-generated prescriptions, and provides a diagnostic chat feature for psychologists.
- **Technologies used:** Node.js, Express.js, PostgreSQL, React.js, OpenAI API, Nearbyy API, Axios, Cors, Dotenv.
- **Challenges faced:** Ensuring secure and seamless data handling and managing real-time API integration for prescriptions and diagnostics.
- **Future improvements:** Implementing secure user authentication, advanced AI models, and multilingual support.

## **Table of Contents**
1. [Introduction](#introduction)
2. [Project Description](#project-description)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Additional Documentation](#additional-documentation)
6. [License](#license)
7. [Status Badges](#status-badges)

## **Installation**
### Prerequisites
- **Node.js** - [Download here](https://nodejs.org/)
- **npm or yarn** - Included with Node.js installation
- **PostgreSQL** - [Download here](https://www.postgresql.org/download/)
- **OpenAI API Key** - [Get API key](https://platform.openai.com/account/api-keys)
- **Nearbyy API Key** - [Get API key](https://docs.nearbyy.com/)

### Backend Setup
1. **Clone the repository:**
    ```bash
    git clone https://github.com/ivmg5/User-Integration.git
    ```
2. **Navigate to the backend directory:**
    ```bash
    cd User-Integration/backend
    ```
3. **Install dependencies:**
    ```bash
    npm install
    ```
4. **Configure environment variables:**
   Create a `.env` file in the backend directory:
    ```plaintext
    OPENAI_API_KEY=your_openai_api_key
    NEARBYY_API_KEY=your_nearbyy_api_key
    ```
5. **Set up the database:**
   Configure PostgreSQL connection in `config/db.js` and ensure a database named `catedraapi` is running.
6. **Run the server:**
    ```bash
    node index.js
    ```

### Frontend Setup
1. **Navigate to the frontend directory:**
    ```bash
    cd ../frontend
    ```
2. **Install dependencies:**
    ```bash
    npm install
    ```
3. **Run the frontend application:**
    ```bash
    npm run dev
    ```
4. **Access the application:**
   Open [http://localhost:5173](http://localhost:5173) in your browser.

## **Usage**
### Running the Application
Ensure the backend server (port 3000) and frontend application (port 5173) are both active.

### Key Features
- **Dashboard:** View, search, and register users with essential information (name, email, etc.).
- **Register User:** Use the "Register" feature to add new patient records.
- **User Details:** View and manage patient details, including descriptions, prescriptions, and feedback.
- **AI-Powered Prescription Generation:**
  1. Enter symptoms and click "Generate Prescription."
  2. Save the generated prescription to the user's record.
- **Interactive Chat:** Engage with a chat interface for DSM-5 diagnostic assistance, with context provided by Nearbyy API.

## **Additional Documentation**
For more advanced details, refer to `Documentation.pdf` in the repository.

## **License**
This project is licensed under the MIT License.

## **Status Badges**
[![Build Status](https://img.shields.io/badge/status-active-brightgreen)](#)
[![Code Coverage](https://img.shields.io/badge/coverage-80%25-yellowgreen)](#)
