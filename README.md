# Task Manager Application

A full-stack task management application built with Spring Boot and React. This application allows users to create and manage task lists and tasks with features like priority levels, status tracking, and organized task management.

## 🚀 Features

- **Task Lists Management**: Create, view, update, and delete task lists
- **Task Management**: Manage individual tasks within task lists
- **Priority Levels**: Assign priority levels (LOW, MEDIUM, HIGH, CRITICAL) to tasks
- **Status Tracking**: Track task status (TODO, IN_PROGRESS, DONE, CANCELLED)
- **Modern UI**: Responsive React frontend with NextUI components and Tailwind CSS
- **RESTful API**: Well-structured backend API with Spring Boot
- **Database Persistence**: PostgreSQL database for reliable data storage
- **Dockerized**: Easy deployment with Docker and Docker Compose

## 🛠️ Tech Stack

### Backend
- **Java 17**
- **Spring Boot 3.5.7**
- **Spring Data JPA**
- **PostgreSQL**
- **Maven**

### Frontend
- **React 18**
- **TypeScript**
- **Vite**
- **NextUI**
- **Tailwind CSS**
- **React Router**
- **Axios**
- **Framer Motion**

### DevOps
- **Docker**
- **Docker Compose**

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Java 17** or higher
- **Node.js** (v18 or higher) and npm
- **Maven** (v3.6 or higher)
- **Docker** and **Docker Compose**
- **PostgreSQL** (if not using Docker)

## 🔧 Installation & Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
cd TaskManagerApp
```

### 2. Backend Setup

#### Configure Database

The application uses PostgreSQL. Update the database configuration in `src/main/resources/application.properties` if needed:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5433/taskdb?serverTimezone=Asia/Kolkata
spring.datasource.username=postgres
spring.datasource.password=mishGill
```

#### Build the Backend

```bash
./mvnw clean install
```

### 3. Frontend Setup

Navigate to the Frontend directory and install dependencies:

```bash
cd Frontend
npm install
```

## 🚀 Running the Application

### Option 1: Using Docker Compose (Recommended)

The easiest way to run the entire application:

1. **Start the Database:**
```bash
docker-compose up -d
```

2. **Run the Backend:**
```bash
./mvnw spring-boot:run
```

3. **Run the Frontend:**
```bash
cd Frontend
npm run dev
```

The application will be available at:
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:8080
- **PostgreSQL**: localhost:5432

### Option 2: Manual Setup

1. **Start PostgreSQL Database:**
```bash
docker-compose up db -d
```

2. **Run the Spring Boot Backend:**
```bash
./mvnw spring-boot:run
```

3. **Run the React Frontend:**
```bash
cd Frontend
npm run dev
```

## 📚 API Endpoints

### Task Lists

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/tasklists` | Get all task lists |
| GET | `/api/tasklists/{id}` | Get a specific task list |
| POST | `/api/tasklists` | Create a new task list |
| PUT | `/api/tasklists/{id}` | Update a task list |
| DELETE | `/api/tasklists/{id}` | Delete a task list |

### Tasks

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/tasks` | Get all tasks |
| GET | `/api/tasks/{id}` | Get a specific task |
| POST | `/api/tasks` | Create a new task |
| PUT | `/api/tasks/{id}` | Update a task |
| DELETE | `/api/tasks/{id}` | Delete a task |

## 📁 Project Structure

```
TaskManagerApp/
├── src/main/java/com/jimmy/TaskManager/
│   ├── controllers/          # REST API Controllers
│   ├── domain/
│   │   ├── dto/             # Data Transfer Objects
│   │   └── entities/        # JPA Entities
│   ├── mappers/             # Entity-DTO Mappers
│   ├── repositories/        # JPA Repositories
│   └── services/            # Business Logic Services
├── Frontend/
│   └── src/
│       ├── components/      # React Components
│       ├── domain/          # TypeScript Models
│       └── assets/          # Static Assets
├── docker-compose.yml       # Docker Compose Configuration
└── pom.xml                  # Maven Configuration
```

## 🏗️ Architecture

The application follows a layered architecture:

1. **Presentation Layer**: React components and REST controllers
2. **Service Layer**: Business logic implementation
3. **Data Access Layer**: JPA repositories and entities
4. **Database Layer**: PostgreSQL database

## 🧪 Testing

Run backend tests:
```bash
./mvnw test
```

Run frontend linting:
```bash
cd Frontend
npm run lint
```

## 🤝 Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**[Jimmy](https://github.com/Yash-Raj-5424)**

## 🙏 Acknowledgments

- Spring Boot team for the excellent framework
- React team for the amazing frontend library
- NextUI for beautiful UI components
- All contributors who help improve this project
