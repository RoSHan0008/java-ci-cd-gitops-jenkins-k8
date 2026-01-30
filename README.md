# 🚀 End-to-End Java CI/CD Pipeline with GitOps

![Project Banner](spring-boot-app/img/project-banner.png)

[![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=Jenkins&logoColor=white)](https://www.jenkins.io/)
[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![ArgoCD](https://img.shields.io/badge/Argo%20CD-ef7b4d?style=for-the-badge&logo=argo-cd&logoColor=white)](https://argoproj.github.io/cd/)
[![Helm](https://img.shields.io/badge/Helm-0F1628?style=for-the-badge&logo=helm&logoColor=white)](https://helm.sh/)
[![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/)

## 📝 Overview
This project demonstrates a robust, enterprise-grade **Continuous Integration and Continuous Deployment (CI/CD)** pipeline for a Java-based Spring Boot application. It leverages modern **GitOps** principles using Jenkins for automation, SonarQube for code quality, and Argo CD for automated deployments to Kubernetes.

## 🛠 Tech Stack
- **Spring Boot**: Underlying Java web application framework.
- **Maven**: Build and dependency management.
- **Jenkins**: Orchestrates the CI pipeline.
- **SonarQube**: Static Application Security Testing (SAST).
- **Docker**: Containerization of the application.
- **Argo CD**: GitOps tool for continuous delivery to Kubernetes.
- **Helm**: Package manager for Kubernetes manifests.
- **Kubernetes**: Container orchestration platform.

## 🏗 Pipeline Architecture
1. **Checkout**: Pulling source code from Git.
2. **Build & Test**: Compiling Java code and running unit tests via Maven.
3. **Static Analysis**: Code quality check using SonarQube.
4. **Containerization**: Building a Docker image and pushing it to a registry.
5. **GitOps Update**: Updating Helm charts/manifests in Git to trigger Argo CD.
6. **Deployment**: Argo CD synchronizes the cluster state with the Git repository.

## 🚀 Getting Started

### Prerequisites
- Docker installed
- Kubernetes cluster (Minikube/EKS/GKE)
- Jenkins instance with Docker and Maven plugins

### Local Execution (Docker)
To run the application locally using Docker:
```bash
docker build -t java-app:v1 ./spring-boot-app
docker run -d -p 8080:8080 java-app:v1
```

## 📂 Project Structure
- `spring-boot-app/`: Source code for the Java application.
- `spring-boot-app-manifests/`: Kubernetes deployment manifests used by Argo CD.
- `Jenkinsfile`: Defines the automated pipeline stages.

---
*Created by [Roshan Kumar Singh](https://github.com/RoSHan0008) | [Website](https://roshankumarsingh.in)*
