# Spring Boot Docker Application

A production-ready Spring Boot application with Docker support.

## Prerequisites

- Java 17+
- Maven 3.6+
- Docker & Docker Compose

## Quick Start

### Local Development

```bash
# Run with Maven
mvn spring-boot:run

# Run tests
mvn test
```

### Docker

```bash
# Build and run with Docker Compose
docker-compose up --build

# Run in detached mode
docker-compose up -d

# View logs
docker-compose logs -f

# Stop containers
docker-compose down
```

### Build Docker Image Manually

```bash
# Build image
docker build -t spring-boot-app:latest .

# Run container
docker run -p 8080:8080 spring-boot-app:latest
```

## GitHub Actions

The project includes a CI/CD pipeline that:
- Builds the application with Maven
- Runs tests
- Builds and pushes Docker images to Docker Hub

### Setup

Add these secrets to your GitHub repository:
- `DOCKER_USERNAME`: Your Docker Hub username
- `DOCKER_PASSWORD`: Your Docker Hub password/token

## API Endpoints

- Health check: `GET http://localhost:8080/actuator/health`
- Your endpoints here...

## Environment Variables

- `SPRING_PROFILES_ACTIVE`: Active Spring profile (default: dev)
- `SPRING_DATASOURCE_URL`: Database URL
- `SPRING_DATASOURCE_USERNAME`: Database username
- `SPRING_DATASOURCE_PASSWORD`: Database password

## Project Structure

```
.
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
├── .github/
│   └── workflows/
│       └── docker-build.yml
├── Dockerfile
├── docker-compose.yml
├── pom.xml
└── README.md
```

# Quick Start Commands
```bash
docker-compose up --build- Build and start all services
```
```bash
mvn spring-boot:run- Run locally without Docker
```
```bash
docker build -t myapp .- Build Docker image manually
```
