# Product Requirements Document

# Go API Gateway

Version: 0.1

Status: Draft

---

# Problem Statement

Modern applications often consist of multiple backend services.

Clients should not communicate directly with every service.

Without an API Gateway:

- Authentication is duplicated
- Logging is duplicated
- Rate limiting is duplicated
- CORS is duplicated
- Services become tightly coupled

A centralized gateway simplifies backend architecture by acting as the single entry point for all incoming requests.

---

# Vision

Build a lightweight, developer-friendly API Gateway in Go that demonstrates modern backend engineering concepts while remaining easy to understand and extend.

---

# Goals

Primary Goals

- Learn Go through a real-world project.
- Understand networking and HTTP internals.
- Learn middleware architecture.
- Build reusable infrastructure.
- Showcase backend engineering skills.

Secondary Goals

- Support multiple backend services.
- Be configurable.
- Be Docker-friendly.
- Be easy to contribute to.

---

# Target Users

Primary

Backend Engineers

Students

Developers learning Go

Open Source Contributors

Secondary

Small startups

Internal developer teams

---

# Functional Requirements

### Routing

The gateway must route requests to backend services based on URL patterns.

---

### Reverse Proxy

The gateway must forward requests while preserving:

- Headers
- Query Parameters
- HTTP Method
- Response

---

### Middleware

Support middleware chain.

Examples

- Logger
- JWT
- Rate Limiter
- CORS
- Recovery

---

### Configuration

Services should be configurable through YAML.

Example

```yaml
routes:
  auth:
    path: /auth
    target: http://localhost:9001
```

---

### Health Checks

Provide:

/health

/ready

/live

---

### Logging

Support structured logging.

---

### Authentication

JWT validation.

---

### Rate Limiting

IP-based.

Future:

Redis-backed.

---

### Metrics

Expose Prometheus metrics.

---

# Non-functional Requirements

Fast startup.

Minimal dependencies.

Easy to extend.

Docker compatible.

Clean architecture.

Readable code.

---

# Out of Scope

Authentication Provider

OAuth Server

Kubernetes Controller

API Documentation Generator

GraphQL Gateway

Service Mesh

---

# Success Metrics

Gateway successfully routes requests.

Response latency remains low.

Configuration is simple.

New middleware can be added with minimal changes.

Documentation allows contributors to understand the project.

---

# Milestones

## v0.1

HTTP Server

Router

Reverse Proxy

---

## v0.2

Configuration

Logger

Recovery

---

## v0.3

JWT

---

## v0.4

Rate Limiter

---

## v0.5

Redis

---

## v0.6

Metrics

---

## v0.7

Load Balancer

---

## v1.0

Stable Release