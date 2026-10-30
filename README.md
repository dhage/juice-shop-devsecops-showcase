# DevSecOps Showcase with OWASP Juice Shop

![Dependency Check](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/dependency-check.yml/badge.svg)
![SAST Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/sast.yml/badge.svg)
![Container Security Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/trivy.yml/badge.svg)

## Overview

This project demonstrates the implementation of a modern DevSecOps pipeline using OWASP Juice Shop.

The goal is to integrate security controls across the entire software delivery lifecycle.

## Local Setup

### Start with Docker

```bash
docker compose up -d
```

Application:

[http://localhost:3000](http://localhost:3000)

## Technologies

- OWASP Juice Shop
- Docker
- GitHub Actions
- Semgrep
- Trivy
- OWASP Dependency Check
- Kubernetes
- Terraform
- Prometheus
- Grafana

## Security Controls

### Software Composition Analysis (SCA)

- OWASP Dependency Check

Third-party dependencies are automatically analyzed for known security vulnerabilities.

### SAST
- Semgrep

### Dependency Scanning
- OWASP Dependency Check

### Container Security

- Trivy

Container images are automatically scanned for known vulnerabilities (CVEs) during every push.

### CI/CD
- GitHub Actions

### Infrastructure as Code
- Terraform

### Container Orchestration
- Kubernetes

## Security Scanning

### SAST

This project uses Semgrep to perform static application security testing (SAST) during every pull request and push event.

Security findings are automatically detected in the CI/CD pipeline.

## Pipeline Vision

Developer
→ GitHub
→ GitHub Actions
→ Security Scans
→ Docker Build
→ Container Scan
→ Kubernetes Deployment

