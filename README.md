# Kwora: A Quora-like Q&A Platform

Kwora is a modern, scalable Q&A platform inspired by Quora, built with Go and microservices architecture. It provides a robust platform for users to ask questions, share knowledge, and engage in meaningful discussions.

## 🚀 Features

- **User Management**: Complete user authentication and profile management
- **Q&A System**: Ask questions, provide answers, and engage in discussions
- **Article System**: Create and share long-form content
- **Social Features**: Follow users, like content, and interact with others
- **Real-time Chat**: Direct messaging between users
- **Search**: Advanced search capabilities powered by Elasticsearch
- **Content Moderation**: Built-in content moderation system

## 🛠 Tech Stack

- **Backend Framework**: [go-zero](https://github.com/zeromicro/go-zero) - A cloud-native Go microservices framework
- **Database**: 
  - MySQL (via GORM)
  - Redis for caching
- **Search Engine**: Elasticsearch
- **Message Queue**: Kafka
- **Service Discovery**: Consul
- **Storage**: Aliyun OSS
- **Container Orchestration**: Kubernetes
- **Authentication**: JWT
- **Tracing**: OpenTelemetry

## 📁 Project Structure

```
.
├── application/           # Main application services
│   ├── article/          # Article service
│   ├── chat/            # Chat service
│   ├── follow/          # Follow service
│   ├── like/            # Like service
│   ├── member/          # Member service
│   ├── message/         # Message service
│   ├── qa/              # Q&A service
│   └── user/            # User service
├── pkg/                  # Shared packages
├── db/                   # Database migrations and schemas
├── .github/             # GitHub workflows and templates
└── k8s/                 # Kubernetes deployment files
```

## 🚀 Getting Started

### Prerequisites

- Go 1.21.0 or later
- Docker and Docker Compose
- Kubernetes cluster (for production deployment)
- MySQL 8.0+
- Redis
- Elasticsearch 8.x
- Kafka
- Consul

### Development Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/eugenescat/kwora-platform.git
   cd kwora-platform
   ```

2. Install dependencies:
   ```bash
   go mod download
   ```

3. Set up the development environment:
   ```bash
   # Start required services using Docker Compose
   docker-compose up -d
   ```

4. Run the services:
   ```bash
   # Start individual services
   go run application/user/api/user.go
   go run application/article/api/article.go
   # ... other services
   ```

### Production Deployment

1. Build Docker images:
   ```bash
   docker build -f user-rpc.dockerfile -t kwora/user-rpc .
   docker build -f article-rpc.dockerfile -t kwora/article-rpc .
   # ... build other services
   ```

2. Deploy to Kubernetes:
   ```bash
   kubectl apply -f k8s/
   ```

## 📝 API Documentation

API documentation is available at `/api/docs` when running the services locally.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



