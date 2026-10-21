# Eureka Server

A Netflix Eureka service registry for the microservices of this practice project. Services register here, and other services (and the gateway) find them by name instead of by fixed addresses.

## Tech stack

- Java 17
- Spring Boot 3.3.2
- Spring Cloud 2023.0.3 (Netflix Eureka Server)
- Spring Boot Actuator
- Maven

## Configuration

| Setting | Value |
|---|---|
| Application name | `eureka-server` |
| Port | `8761` |
| Fetch registry | `false` (the server does not fetch from another registry) |
| Register with Eureka | `false` (the server does not register itself) |

## Run locally

The application is in the `eureka-server` folder.

```bash
cd eureka-server
mvn spring-boot:run
```

Open the dashboard at http://localhost:8761 to see the registered services.

## Related repositories

- [config-server](https://github.com/danishahm89/config-server): centralized configuration
- [cloud-config](https://github.com/danishahm89/cloud-config): the configuration files
- [api-gateway](https://github.com/danishahm89/api-gateway): registers here and routes requests to services by name

## Concepts shown

- Service discovery and registration with Eureka
- Client-side load balancing by service name
