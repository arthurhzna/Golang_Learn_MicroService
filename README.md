# Learning Microservices with Go

This repository was created to document my learning progress from the course:  
👉 [Working with Microservices in Go (Udemy)](https://www.udemy.com/course/working-with-microservices-in-go/)

This repository contains a Go implementation of microservices I built to learn microservices architecture. The project consists of several independent services that communicate with each other.

## 🚀 Core Services

### Main Services
- **authentication-service** - Authentication service with PostgreSQL
- **broker-service** - Main entry point connecting all services
- **logger-service** - Centralized logging system with MongoDB
- **listener-service** - RabbitMQ message consumer
- **mail-service** - Email sender with templates

### Supporting Infrastructure
- **front-end** - Simple user interface
- **project/** - Docker and Kubernetes configurations

## 🛠️ Project Structure

```
Golang_Learn_Micro_Service/
├── authentication-service/    # Authentication service
│   ├── cmd/                   # Main code
│   ├── data/                  # Data models
│   ├── go.mod                 # Dependencies
│   └── users.sql              # Database schema
├── broker-service/            # Entry point
├── listener-service/          # Message consumer
├── logger-service/            # Logging system
├── mail-service/              # Email service
└── project/                   # Deployment
    ├── docker-compose.yml     # Container configuration
    └── k8s/                   # Kubernetes configuration
```

## 💻 Getting Started

### Prerequisites
- Go 1.18+
- Docker
- GNU Make

### Running the Project
```bash
# Build and run all containers
make up_build

# Run the front-end
make start

# Run specific service (e.g., auth)
make auth
```

### Useful Commands
```bash
# View all make commands
make help

# Stop all containers
make down

# Clean binaries
make clean
```

## 📚 What I Learned
- Microservices architecture with Go
- Inter-service communication using:
  - REST API (JSON)
  - gRPC
  - RabbitMQ (AMQP)
- Service discovery with etcd
- Containerization with Docker
- Orchestration with Kubernetes

## 🔧 Key Technologies
- **Databases**: PostgreSQL, MongoDB
- **Message Broker**: RabbitMQ
- **Container**: Docker
- **Orchestration**: Kubernetes
