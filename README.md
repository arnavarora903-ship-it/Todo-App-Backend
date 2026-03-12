# Todo App Backend

Backend API for a full-stack Todo application built with FastAPI and PostgreSQL.

This project was completed as part of a course where the application code was provided. The main goal was to learn how to set up a backend server, connect it to a PostgreSQL database, apply database migrations, test API routes locally, and deploy the backend and database to the cloud using Render.

## What I Learned

Through this project, I learned how the major backend pieces work together in a real full-stack setup. I understood how FastAPI is used to build API routes, how Uvicorn runs the backend server and accepts incoming requests, how SQLAlchemy allows Python code to communicate with a PostgreSQL database, how Alembic keeps track of structured database changes through migrations, and how Render can be used to deploy both the backend service and the database online.

## Tech Stack

- Python
- FastAPI
- Uvicorn
- PostgreSQL
- SQLAlchemy
- Alembic
- Render

## Features

- Create todos
- Read todos
- Delete todos
- Persistent database storage
- Backend deployment on Render

## Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/arnavarora903-ship-it/Todo-App-Backend
cd Todo-App-Backend

python -m venv venv

venv\Scripts\activate

.\venv\Scripts\Activate.ps1

pip install -r requirements.txt

Create a .env file and add the database configuration required by the backend. The exact variable names may depend on the project setup, but they typically include the database host, port, name, user, and password.

DATABASE_HOST=...
DATABASE_PORT=...
DATABASE_NAME=...
DATABASE_USER=...
DATABASE_PASSWORD=...

alembic upgrade head

uvicorn app.main:app --reload

API Testing

After starting the backend server, the API can be tested locally using FastAPI’s interactive documentation, a browser for simple routes, or tools like Postman. If enabled in the project, the Swagger documentation is usually available at http://127.0.0.1:8000/docs.

Deployment

The backend server and PostgreSQL database were deployed using Render. The deployment process included connecting the GitHub repository to Render, setting the required environment variables, linking the backend to the hosted PostgreSQL database, and verifying that deployed API routes such as GET, POST, and DELETE were working successfully.

Notes

This repository reflects a guided course project where the application code was provided for learning purposes. The main focus of the work was understanding backend setup, database connectivity, migrations, local testing, and deployment workflow rather than building the application logic entirely from scratch.

Author

Arnav Arora
