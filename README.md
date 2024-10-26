RuleEngine

A simple 3-tier rule engine application using Abstract Syntax Tree (AST) to determine user eligibility based on attributes like age, department, income, and spend.

Table of Contents

Overview
Features
Technology Stack
Prerequisites
Installation
Running the Application
API Endpoints
Design Choices
Project Structure

OVERVIEW

This application offers a rule engine that utilizes Abstract Syntax Trees (AST) to represent conditional logic.
It enables the dynamic creation, combination, and modification of these rules, along with the ability to evaluate data based on the defined conditions.

FEATURES

Create rules using a string representation
Combine multiple rules into a single AST
Evaluate data against rules
Simple UI for interacting with the rule engine

TECHNOLOGY STACK

Frontend: React.js
Backend: Node.js with Express.js
Database: MongoDB
State Management: React Hooks

Prerequisites

Before you begin, ensure you have met the following requirements:
Node.js (v14.0.0 or later)
npm (v6.0.0 or later)
MongoDB (v4.0 or later)

Installation

Clone the repository:
Install server dependencies: cd backend npm install
Install client dependencies: cd ../frontend npm install

Running The Application

Start the MongoDB service on your machine.
Start the server: cd server npm start The server will run on http://localhost:5000.
In a new terminal, start the client: cd client npm start
The client will run on http://localhost:3000.
Open your browser and navigate to http://localhost:3000 to use the application.

API Endpoint

POST /api/create-rule: Create a new rule
POST /api/combine-rules: Combine multiple rules
POST /api/evaluate-rule: Evaluate data against a rule






Design Choice

MERN Stack: We chose the MERN (MongoDB, Express.js, React.js, Node.js) stack for its flexibility, scalability, and the ability to use JavaScript throughout the stack.
Abstract Syntax Tree (AST): ASTs are used to represent rules because they provide a flexible and powerful way to structure and evaluate complex logical expressions.
Modular Architecture: The backend is structured with separate routes, models, and utility functions for better organization and maintainability.
React Hooks: We use React Hooks for state management in the frontend, providing a clean and efficient way to handle component state and side effects.
RESTful API: The backend exposes a RESTful API, making it easy to interact with the rule engine from various clients.
MongoDB: MongoDB was chosen as the database for its flexibility in storing complex data structures like ASTs.
Error Handling: Comprehensive error handling is implemented both in the frontend and backend to provide clear feedback to users and developers.
Minimal UI Design: The frontend uses a clean, minimal design to focus on functionality while maintaining good user experience.

Project Structure

rule-engine-ast/ ├── frontend/ │ ├── public/ │ ├── src/ │ │ ├── components/ │ │ ├── App.js │ │ ├── App.css │ │ └── index.js │ └── package.json ├── backend/ │ ├── models/ │ ├── routes/ │ ├── utils/ │ ├── config.js │ ├── server.js │ └── package.json └── README.md