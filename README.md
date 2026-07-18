# go-api-gateway



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