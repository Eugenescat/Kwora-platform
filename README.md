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
- **Service Discovery**: Etcd
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



