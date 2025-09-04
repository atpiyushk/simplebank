# Full-Stack Banking Application

A complete banking backend service built with Go, featuring secure account management, money transfers, and real-time transaction processing with production-ready deployment on AWS.

## Overview

This project demonstrates professional-grade backend development for a banking service, providing RESTful HTTP APIs and gRPC endpoints for account management, secure money transfers, and comprehensive transaction tracking.

## Features

- **Account Management**: Create and manage bank accounts with multi-currency support
- **Money Transfers**: ACID-compliant transfers between accounts with deadlock prevention
- **Authentication**: JWT/PASETO tokens with refresh token sessions and RBAC
- **Background Processing**: Async email verification and task processing with Redis
- **Production Ready**: Docker containerization, Kubernetes deployment, and CI/CD with GitHub Actions

## Tech Stack

**Backend**: Go, Gin, PostgreSQL, Redis, SQLC, gRPC  
**Infrastructure**: Docker, Kubernetes (AWS EKS), AWS RDS, AWS ECR  
**Security**: Bcrypt, JWT/PASETO, TLS with Let's Encrypt  
**DevOps**: GitHub Actions, AWS Secrets Manager, Route53

### Setup
```bash
# Clone and setup infrastructure
git clone https://github.com/atpiyushk/banking-app.git
cd banking-app
make network && make postgres && make createdb && make migrateup

# Generate code and start server
make sqlc && make mock
make server
```

## Database Schema

**Core Tables**: users, accounts, entries, transfers, sessions  
**Features**: Foreign keys, constraints, transaction isolation, migration support

## Security Features

- Bcrypt password hashing
- JWT/PASETO stateless authentication  
- SQL injection protection with SQLC
- Rate limiting and CORS policies
- TLS/HTTPS with automatic certificate renewal

## License

MIT License