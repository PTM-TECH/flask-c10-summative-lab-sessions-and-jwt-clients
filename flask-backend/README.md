# Project title: Expense Tracker API - Flask Session-Based Backend

# Project Description
- This project is a secure RESTful API built using Flask that allows users to manage personal expenses. The system implements session-based authentication, ensuring that each user can only access and manage their own data.

- The API supports full CRUD operations for expenses, pagination for listing records, and secure route protection using Flask sessions.

# Key Features
- User registration and login
- Session-based authentication
- Secure password hashing using Flask-Bcrypt
- Expense management (Create, Read, Update, Delete)
- Pagination for expense listing
- Ownership-based access control (users only access their own expenses)

# Tech Stack
- Python 3.8+
- Flask
- Flask-SQLAlchemy
- Flask-Migrate
- Flask-Bcrypt
- Marshmallow (validation)
- SQLite (default database)

# Installation Instructions
### Clone the repository
- Git clone https://github.com/PTM-TECH/flask-c10-summative-lab-sessions-and-jwt-clients
- cd flask-backend/server

### Create virtual environment
- pipenv install
- pipenv shell

### Install dependencies
- pip install flask flask-sqlalchemy flask-migrate flask-bcrypt marshmallow

### Set up the database
- Initialize migrations: flask db init
- Create migrations: flask db migrate -m"initial migration"
- Apply migrations: flask db upgrade head

### Seed the database(optional)
python3 seed.py

# Run Instructions
- Start the flask server: python3 app.py

# Authentication Endpoints

### /signup -> POST
- Register a new user and create session
### /login -> POST
- Log in a user and create session
### /check_session -> GET
- Check if a user is logged in
### /logout
- Logs out user and clears session

# Expense Endpoints

### /expenses -> GET
- Get all expenses (paginated)
- Example Query params: ?page=1&per_page=10
### /expenses/<int:id> -> GET
- Get a single expense by id.
### /expenses -> POST
- Create a new expense
### /expenses/<int:id> -> PATCH
- Updating an existing expense
### /expenses/<int:id> -> DELETE
- Delete an expense by id

# Security Features
- Passwords are hashed using Flask-Bcrypt
- Session-based authentication
- Protected routes (login required)
- Users can only access their own expenses
- Ownership validation on all expense operations

# Notes
- All endpoints return JSON responses
- Ensure server runs on port 5555 for frontend compatibility
- Database migrations must be applied before running the app

# Author

Patrick Mutua
