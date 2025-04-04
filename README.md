# Node.js PostgreSQL Docker API

This project is a REST API built with Node.js and PostgreSQL, containerized with Docker.

## Prerequisites

- Docker
- Docker Compose

## Project Structure

```
backend/
├── .env                  # Environment variables
├── .dockerignore        # Docker ignore file
├── docker-compose.yml   # Docker compose configuration
├── Dockerfile           # Docker configuration for Node.js app
├── index.js            # Main application file
├── init.sql            # Database initialization
├── package.json        # Node.js dependencies
└── README.md           # This file
```

## Environment Variables

Create a `.env` file with the following variables:

```
DB_USER=postgres
DB_PASSWORD=postgres
DB_NAME=mydatabase
PORT=3000
```

## Getting Started

1. Clone the repository:
```bash
git clone [your-repository-url]
cd backend
```

2. Start the application:
```bash
docker-compose up --build
```

3. The API will be available at:
- http://localhost:3000/users

## API Endpoints

- GET `/users` - Returns a list of users

## Database

The PostgreSQL database is automatically initialized with a `users` table and sample data.

## Docker Commands

```bash
# Start the application
docker-compose up --build

# Stop the application
docker-compose down

# View logs
docker-compose logs

# Remove volumes (to reset the database)
docker volume rm backend_postgres_data
``` 