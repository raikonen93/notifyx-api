# NotifyX API

![Build](https://github.com/raikonen93/notifyx-api/actions/workflows/build.yml/badge.svg)

NotifyX API is a .NET 9 Web API with Serilog, Swagger, and HealthChecks.

## Running locally
```bash
dotnet restore
dotnet run --project Notifyx.Api
```

Available at:
- Swagger: http://localhost:5175/swagger
- Health Live: http://localhost:5175/health/live
- Health Ready: http://localhost:5175/health/ready

## Running with Docker
```bash
docker build -t notifyx-api .
docker run -p 5002:8080 notifyx-api
```

Available at:
- Swagger: http://localhost:5002/swagger

## Environment variables (unified across services)
Set these variables for local development and containers as needed.

```bash
# ASP.NET Core
ASPNETCORE_ENVIRONMENT=Development

# PostgreSQL
ConnectionStrings__Postgres=Host=postgres;Port=5432;Database=parkydb;Username=admin;Password=admin

# Redis
ConnectionStrings__Redis=redis:6379

# RabbitMQ
RabbitMQ__HostName=rabbitmq
RabbitMQ__Port=5672
RabbitMQ__UserName=guest
RabbitMQ__Password=guest

# MongoDB
ConnectionStrings__Mongo=mongodb://mongo:27017
```
