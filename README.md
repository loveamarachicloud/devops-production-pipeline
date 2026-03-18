# DevOps Production Pipeline
![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Orchestration-blue)
![CI/CD](https://img.shields.io/badge/CI/CD-GitHub_Actions-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

Dockerized application deployed on Kubernetes with automated CI/CD pipeline using GitHub Actions and Docker Hub.

---

## Project Overview

This project demonstrates how to build, containerize, and deploy a web application using a complete DevOps workflow.

It covers:

- Docker image creation
- Kubernetes deployment using Minikube
- Service exposure using NodePort
- CI/CD pipeline using GitHub Actions
- Container image push to Docker Hub

---

## Architecture

![Architecture Diagram](screenshots/architecture.png)

---

## Technology Stack

- Docker
- Kubernetes
- Minikube
- kubectl
- GitHub Actions
- Docker Hub
- Nginx

---

## Project Features

- Dockerized web application
- Kubernetes deployment with multiple pods
- Service exposure using NodePort
- Application scaling demonstration
- Kubernetes self-healing test
- Automated CI/CD pipeline with GitHub Actions

---

## Quick Start

### 1. Start Minikube
```bash
minikube start
```
### 2. Build Docker Image
```bash
docker build -f docker/Dockerfile -t devops-pipeline-app .
```
### 3. Deploy to Kubernetes
```bash
kubectl apply -f k8s/deployment.yaml```
kubectl apply -f k8s/service.yaml
```
### 4. Verify Pods
```bash
kubectl get pods
```
### 5. Access the Application
```bash
minikube service nginx-service
```
## Application Running in Kubernetes

The application is deployed to a local Kubernetes cluster using Minikube and exposed through a Kubernetes Service.
## CI/CD Pipeline

This project uses GitHub Actions to automate the deployment workflow.

Pipeline stages:

- Build Docker image
- Push image to Docker Hub
- Prepare for Kubernetes deployment

Workflow file:

```bash
.github/workflows/docker-build.yml
```

## Project Roadmap

Planned improvements:

Add Helm charts for packaging Kubernetes deployments

Implement ArgoCD for GitOps deployment

Integrate Prometheus for monitoring

Add Grafana dashboards

Improve CI/CD pipeline with testing and validation

Add troubleshooting and operational documentation