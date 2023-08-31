
# Specs

Database: Postgresql\
Framework: Express.js\
Language: Typescript

# Set Up

1-Create .env file in root directory and set db-uri value to your database url

2-Compile the typescript files to javascript files:

```bash
  npm run build
```

3-Run the server:

```bash
  npm run start
```

# Unit Testing

```bash
  npm run test
```

# Endpoints

### POST /api/tasks
Creates a new task with given properties.

Request Body: 
```json
  {
      "title": string,
      "description": string,
      "dueDate": string ( ISO 8601 date format)
  }
```

returns the created task object in JSON format (with "id" property)

### GET /api/tasks/{taskId}

returns the the task object in JSON format.

### PUT /api/tasks/{taskId}

Updates the task with the given properties in request body:

Request Body: 
```json
  {
      "title": string,
      "description": string,
      "dueDate": string ( ISO 8601 date format)
  }
```

### DELETE /api/tasks/{taskId}

Deletes the task with the given id.

