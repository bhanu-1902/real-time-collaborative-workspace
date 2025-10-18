# 🚀 Real-Time Collaborative Workspace Platform

A modern collaborative workspace platform that combines project management, real-time document collaboration, and team communication - similar to a simplified Notion meets Slack with project tracking capabilities.

## 🎯 Project Overview

**Goal**: Build a modern collaborative workspace platform with real-time collaboration capabilities

**Tech Stack**:
- **Frontend**: React 18 + TypeScript + Apollo Client + Material-UI
- **Backend**: Spring Boot 3.2+ + GraphQL + Java 17
- **Database**: Oracle Database 19c + Redis (caching + pub/sub)
- **Real-time**: WebSocket + GraphQL Subscriptions
- **Deployment**: Docker + Kubernetes

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Node.js 18+
- Java 17+
- Maven 3.8+

### Local Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/bhanu-1902/real-time-collaborative-workspace.git
   cd real-time-collaborative-workspace
   ```

2. **Start the development environment**
   ```bash
   docker-compose up -d
   ```

3. **Access the applications**
   - Frontend: http://localhost:3000
   - Backend: http://localhost:8080
   - GraphQL Playground: http://localhost:8080/graphiql
   - Database: Oracle DB on port 1521
   - Redis: localhost:6379

4. **Run tests**
   ```bash
   # Backend tests
   cd backend && mvn test
   
   # Frontend tests
   cd frontend && npm test
   ```

## 📁 Project Structure

```
real-time-collaborative-workspace/
├── backend/                 # Spring Boot GraphQL API
│   ├── src/main/java/
│   ├── src/main/resources/
│   └── pom.xml
├── frontend/               # React TypeScript App
│   ├── src/
│   ├── public/
│   └── package.json
├── docker/                 # Docker configurations
│   ├── oracle/
│   └── redis/
├── kubernetes/             # K8s deployment manifests
├── docs/                   # Project documentation
├── .github/               # GitHub workflows and templates
└── docker-compose.yml     # Local development setup
```

## 🔄 Development Workflow

### Branch Strategy
- `master`: Production-ready code
- `develop`: Integration branch for features
- `feature/*`: Feature development branches
- `hotfix/*`: Critical bug fixes
- `release/*`: Release preparation branches

### Pull Request Process
1. Create feature branch from `develop`
2. Implement feature with tests
3. Create PR with template completion
4. Code review and approval (2 reviewers required)
5. Merge after all checks pass

## 📊 Key Features

- **🏢 Workspace Management**: Multi-tenant workspaces with role-based access
- **📋 Project Management**: Kanban boards with drag-and-drop functionality
- **⚡ Real-time Collaboration**: Live updates via GraphQL subscriptions
- **📁 File Management**: Upload, versioning, and secure access control
- **🔐 Authentication**: JWT-based auth with refresh tokens
- **📈 Performance**: Redis caching and query optimization
- **🔍 Monitoring**: Comprehensive observability with metrics and logging

## 🏗️ Architecture

### Backend Architecture
- **Spring Boot 3.2+**: Modern Java framework with reactive support
- **GraphQL**: Type-safe API with real-time subscriptions
- **Oracle Database**: Robust relational database with proper indexing
- **Redis**: Caching layer and pub/sub for real-time features
- **JWT Security**: Stateless authentication with role-based access

### Frontend Architecture
- **React 18**: Latest React with concurrent features
- **TypeScript**: Type safety and better developer experience
- **Apollo Client**: GraphQL client with caching and subscriptions
- **Material-UI**: Professional UI component library
- **React Router**: Client-side routing

## 🔧 Development Commands

### Backend (Spring Boot)
```bash
cd backend
mvn spring-boot:run          # Start development server
mvn test                     # Run tests
mvn package                  # Build JAR
mvn spotless:apply          # Format code
```

### Frontend (React)
```bash
cd frontend
npm start                    # Start development server
npm test                     # Run tests
npm run build               # Build for production
npm run lint                # Lint code
```

## 📈 Performance Targets

- **Response Time**: p95 < 200ms for critical operations
- **Concurrent Users**: Support 1000+ simultaneous users
- **Availability**: 99.9% uptime target
- **Cache Hit Ratio**: >70% for frequently accessed data

## 🛡️ Security

- JWT authentication with refresh tokens
- Role-based access control (RBAC)
- Rate limiting and CSRF protection
- Input validation and sanitization
- Audit logging for all operations
- OWASP Top 10 compliance

## 📚 Documentation

- [API Documentation](docs/api.md)
- [Architecture Guide](docs/architecture.md)
- [Deployment Guide](docs/deployment.md)
- [Contributing Guidelines](CONTRIBUTING.md)
- [Security Policy](SECURITY.md)

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🎯 Interview Preparation

This project demonstrates:
- **System Design**: Scalable architecture with microservices patterns
- **Real-time Systems**: WebSocket implementation with GraphQL subscriptions
- **Performance Optimization**: Caching strategies and query optimization
- **Security**: Authentication, authorization, and data protection
- **DevOps**: CI/CD, containerization, and monitoring

---

*Built with ❤️ for learning system design and modern full-stack development*