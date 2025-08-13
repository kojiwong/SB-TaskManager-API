# Task Manager API
A simple yet powerful REST API for managing your tasks. Built using Spring Boot, PostgreSQL, and an embedded Tomcat server.

## Overview
Task Manager API is a backend service that lets you create, update, delete, and retrieve tasks.
This project was great for learning Spring Boot, Spring Data JPA, and PostgreSQL in a real-world style project.

## Features:

- Create tasks with titles, descriptions, and due dates

- List all tasks or fetch a specific one

- Update task details and mark them complete/incomplete

- Delete tasks when they’re done (or if you give up 😅)

- RESTful API ready to integrate with any frontend


## How to Run

### Install Required Tools
Make sure you have:
- Java 17+

- Maven

- PostgreSQL

### Check if versions are good
```
java -version
mvn -version
psql --version
```

### Create database in postgres
```
psql -U postgres
CREATE DATABASE taskdb;
\q
```

### Run the command to start server
```
mvn spring-boot:run
```

Server can be accessed at [localhost:8080](http://localhost:8080)

### API endpoints
| Method |	Endpoint |	Description |
| ------ | --------- | ------------ |
| GET |	/api/tasks |	Get all tasks |
| GET |	/api/tasks/{id} |	Get task by ID |
| POST |	/api/tasks |	Create new task |
| PUT |	/api/tasks/{id} |	Update task |
| DELETE |	/api/tasks/{id} |	Delete task |

### Create an example task
```
curl -X POST http://localhost:8080/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title":"Buy groceries","description":"Milk, Eggs","dueDate":"2025-06-20"}'
```

### Get tasks
```
curl http://localhost:8080/api/tasks
```
