# Go API Gateway

> A lightweight, configurable API Gateway built in Go for modern microservices.

![Go Version](https://img.shields.io/badge/Go-1.24+-00ADD8)
![License](https://img.shields.io/badge/license-MIT-green)

## Overview

Go API Gateway is an open-source API Gateway designed to sit between clients and backend services.

It provides a single entry point for applications while handling common cross-cutting concerns such as routing, authentication, logging, rate limiting, observability, and reverse proxying.

The goal of this project is to learn distributed backend architecture by building production-inspired infrastructure from scratch using only Go's standard library wherever possible.

---

## Features

### Current

- Reverse Proxy
- HTTP Routing
- Configuration via YAML
- Health Check Endpoint

### Planned

- JWT Authentication
- Middleware Pipeline
- Structured Logging
- Request IDs
- CORS
- Rate Limiting
- Redis-backed Rate Limiting
- Metrics (Prometheus)
- Service Discovery
- Load Balancer
- Circuit Breaker

---

## Architecture

```

                Client
                   │
                   ▼
           Go API Gateway
                   │
      ┌────────────┴─────────────┐
      ▼                          ▼
Auth Service               Product Service

```

---

## Why this project?

Most backend applications repeatedly implement:

- Authentication
- Logging
- Rate Limiting
- Routing
- Reverse Proxy
- Health Checks

Instead of duplicating those concerns across services, the API Gateway centralizes them into one component.

---

## Technology Stack

- Go
- net/http
- httputil.ReverseProxy
- Docker
- Docker Compose
- YAML Configuration

Future:

- Redis
- Prometheus
- Grafana

---

## Project Structure

```text
cmd/
internal/
configs/
docs/
tests/
examples/
```

---

## Documentation

- Product Requirements
- High-Level Design
- Low-Level Design
- Roadmap

---

## Roadmap

- [ ] v0.1 HTTP Server
- [ ] v0.2 Reverse Proxy
- [ ] v0.3 Config Loader
- [ ] v0.4 Middleware
- [ ] v0.5 JWT
- [ ] v0.6 Rate Limiter
- [ ] v0.7 Redis
- [ ] v0.8 Metrics
- [ ] v0.9 Load Balancer
- [ ] v1.0 Stable Release

---

## License

MIT


# Folder Structure
```ts

go-api-gateway/
│
├── cmd/
│   └── gateway/
│       └── main.go
│
├── internal/
│   ├── config/
│   │   └── config.go
│   │
│   ├── server/
│   │   └── server.go
│   │
│   ├── router/
│   │   └── router.go
│   │
│   ├── proxy/
│   │   └── reverse_proxy.go
│   │
│   └── middleware/
│       ├── logger.go
│       ├── cors.go
│       └── recovery.go
│
├── configs/
│   └── config.yaml
│
├── docs/
│   ├── PRD.md
│   ├── HLD.md
│   ├── LLD.md
│   └── ROADMAP.md
│
├── tests/
│
├── Dockerfile
├── docker-compose.yml
├── Makefile
├── go.mod
├── go.sum
└── README.md

```