Here's a single-page README.md file for the todo list API project:

```markdown
# Todo List REST API

A simple REST API for managing todo tasks built with Node.js, Express, and SQLite.

## Prerequisites
- Node.js (v12 or higher)
- npm (Node Package Manager)

## Installation and Setup

1. Create and navigate to project directory:
```bash
mkdir todo-api
cd todo-api
```

2. Install dependencies:
```bash
npm init -y
npm install express sqlite3 body-parser
```

3. Project Structure:
```
todo-api/
  ├── db/
  │   └── database.js
  ├── app.js
  └── package.json
```

## Running the Application
Start the server:
```bash
node app.js
```
Server runs at: http://localhost:3000

## API Documentation

### 1. Create Task
- **Endpoint:** POST /tasks
- **Headers:** Content-Type: application/json
- **Body:**
```json
{
    "title": "Buy groceries",
    "description": "Get milk and bread"
}
```
- **Response:** Returns created task with ID

### 2. Get All Tasks
- **Endpoint:** GET /tasks
- **Response:** Returns array of all tasks

### 3. Get Single Task
- **Endpoint:** GET /tasks/:id
- **Response:** Returns single task object

### 4. Update Task Status
- **Endpoint:** PUT /tasks/:id
- **Headers:** Content-Type: application/json
- **Body:**
```json
{
    "status": "completed"
}
```
- **Valid Status Values:** "pending", "in-progress", "completed"

### 5. Delete Task
- **Endpoint:** DELETE /tasks/:id
- **Response:** Success message

## Error Handling
- 400: Bad Request (Invalid input)
- 404: Not Found (Task doesn't exist)
- 500: Server Error

## Database
- SQLite database file (todo.db) creates automatically on first run
- Stores tasks with id, title, description, and status fields



