# Todo App

A full-stack Todo application with CRUD operations, authentication, and database integration.

## Tech Stack

### Frontend
- Angular
- Reactive Forms
- HttpClient for API communication

### Backend
- NestJS (Controllers, Services, Middleware, Guards, Modules)
- JWT Authentication

### Database
- PostgreSQL with Prisma ORM

## Features
- User authentication (JWT)
- Todo CRUD operations
- User-specific todos
- Secure API endpoints

## Getting Started

### Prerequisites
- Node.js (v16 or later)
- npm or yarn
- PostgreSQL database

### Installation

1. Clone the repository
   ```
   git clone https://github.com/dogukanakin/todo-app.git
   cd todo-app
   ```

2. Install dependencies
   ```
   # Install frontend dependencies
   cd client
   npm install
   
   # Install backend dependencies
   cd ../server
   npm install
   ```

3. Setup environment variables
   Create a `.env` file in the server directory with the following variables:
   ```
   DATABASE_URL="postgresql://username:password@localhost:5432/todo_db"
   JWT_SECRET="your-secret-key"
   ```

4. Run database migrations
   ```
   cd server
   npx prisma migrate dev
   ```

5. Start the development servers

   Backend:
   ```
   cd server
   npm run start:dev
   ```

   Frontend:
   ```
   cd client
   npm run start
   ```

## Project Structure

```
todo-app/
├── client/                # Angular frontend
└── server/                # NestJS backend
    ├── src/               # Source code
    └── prisma/            # Prisma schema and migrations
```

## API Endpoints

- `POST /auth/register` - Register a new user
- `POST /auth/login` - Log in a user
- `GET /todos` - Get all todos for the authenticated user
- `GET /todos/:id` - Get a specific todo
- `POST /todos` - Create a new todo
- `PATCH /todos/:id` - Update a todo
- `DELETE /todos/:id` - Delete a todo 