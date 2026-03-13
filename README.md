# Todo App Backend

Backend API for a full-stack Todo application built with FastAPI and PostgreSQL.

This project was completed as part of a course where the core application code was provided. The main goal was to learn how to set up a backend server, connect it to a PostgreSQL database, apply database migrations, test API routes locally, and deploy both the backend and database to the cloud using Render.

## What I Learned

Through this project, I learned how the main backend components work together in a real full-stack setup. I understood how FastAPI is used to build API routes, how Uvicorn runs the backend server and handles incoming requests, how SQLAlchemy allows Python code to communicate with a PostgreSQL database, how Alembic keeps track of structured database changes through migrations, and how Render can be used to deploy both the backend service and the database online.

## Tech Stack

- Python
- FastAPI
- Uvicorn
- PostgreSQL
- SQLAlchemy
- Alembic
- Render
- Git
- GitHub

## Features

- REST-style API routes for todo operations
- Create, read, and delete todos
- PostgreSQL database integration
- Database schema migrations with Alembic
- Local development with auto-reload using Uvicorn
- Cloud deployment on Render

## Live Backend

[View Live Backend](https://todo-app-backend-hn3r.onrender.com)

## Run Locally

Clone the repository:

```bash
git clone https://github.com/arnavarora903-ship-it/Todo-App-Backend.git
cd Todo-App-Backend
```

Create and activate a virtual environment:

```bash
python -m venv venv
venv\Scripts\activate
```

For PowerShell, use:

```powershell
.\venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file and add your database configuration:

```env
DATABASE_HOST=YOUR_DATABASE_HOST
DATABASE_PORT=YOUR_DATABASE_PORT
DATABASE_NAME=YOUR_DATABASE_NAME
DATABASE_USER=YOUR_DATABASE_USER
DATABASE_PASSWORD=YOUR_DATABASE_PASSWORD
```

Apply database migrations:

```bash
alembic upgrade head
```

Start the development server:

```bash
uvicorn app.main:app --reload
```

Then open the local API in your browser at:

```bash
http://127.0.0.1:8000
```

## API Testing

After starting the backend server, the API can be tested locally using FastAPI’s interactive documentation, a browser for simple routes, or tools such as Postman.

If enabled in the project, the Swagger UI is available at:

```bash
http://127.0.0.1:8000/docs
```

## Deployment

The backend server and PostgreSQL database were deployed using Render. The deployment process included connecting the GitHub repository to Render, setting the required environment variables, linking the backend to the hosted PostgreSQL database, and verifying that deployed API routes such as GET, POST, and DELETE were working successfully.

## Acknowledgment

The base project structure and core application code were provided through the course. The main purpose of this project was to gain practical experience with backend setup, database integration, migrations, local API testing, GitHub workflow, and cloud deployment using Render.
