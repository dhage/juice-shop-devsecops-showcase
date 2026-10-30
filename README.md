# DevSecOps Showcase with OWASP Juice Shop

![Dependency Check](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/dependency-check.yaml/badge.svg)
![SAST Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/sast.yaml/badge.svg)
![Container Security Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/trivy.yaml/badge.svg)
![Security Gate](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/security-gate.yaml/badge.svg)

## Overview

This project demonstrates a practical DevSecOps implementation using OWASP Juice Shop.

The objective is to integrate security controls throughout the software delivery lifecycle by combining CI/CD automation, security scanning, container security, and Kubernetes deployment.

---

## Architecture

```text
Developer
    ↓
GitHub Repository
    ↓
GitHub Actions
    ↓
Security Scans
 ├─ Semgrep (SAST)
 ├─ OWASP Dependency Check (SCA)
 └─ Trivy (Container Security)
    ↓
Security Gate
    ↓
Docker Image
    ↓
Kubernetes Deployment
```

---

## Technologies

| Area | Technology |
|--------|------------|
| Application | OWASP Juice Shop |
| Containerization | Docker |
| CI/CD | GitHub Actions |
| SAST | Semgrep |
| Container Security | Trivy |
| Dependency Scanning | OWASP Dependency Check |
| Container Orchestration | Kubernetes |
| Infrastructure as Code | Terraform |
| Monitoring | Prometheus, Grafana |

---

## Local Setup

### Start Application

```bash
docker compose up -d
```

Application URL:

```text
http://localhost:3000
```

---

## Security Controls

### Static Application Security Testing (SAST)

- Semgrep
- Automated execution on every push and pull request
- Early detection of security vulnerabilities

### Software Composition Analysis (SCA)

- OWASP Dependency Check
- Detection of vulnerable third-party dependencies
- CVE identification and reporting

### Container Security

- Trivy
- Container image vulnerability scanning
- Automated security checks during CI/CD execution

---

## Security Governance

A dedicated Security Gate validates the results of all automated security scans before deployment activities can proceed.

### Security Validations

- Semgrep SAST validation
- OWASP Dependency Check validation
- Trivy container vulnerability validation

### Purpose

The Security Gate demonstrates how security controls can be enforced as part of a modern DevSecOps workflow by preventing insecure changes from progressing through the CI/CD pipeline.

---

## Kubernetes Deployment

The Kubernetes manifests are located in the `kubernetes` directory.

### Components

- Deployment
- Service
- Ingress

Example:

```bash
kubectl apply -f kubernetes/
```

---

## Repository Structure

```text
.
├── .github/workflows
│   ├── sast.yaml
│   ├── trivy.yaml
│   └── dependency-check.yaml
│
├── kubernetes
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── security
├── reports
├── terraform
└── README.md
```

---

## Roadmap

- [x] Dockerized OWASP Juice Shop
- [x] GitHub Actions CI/CD
- [x] Semgrep SAST
- [x] Trivy Container Scanning
- [x] OWASP Dependency Check
- [x] Kubernetes Manifests
- [x] Terraform Infrastructure
- [ ] Kubernetes Security Scanning
- [ ] Prometheus Monitoring
- [ ] Grafana Dashboards

---

## Learning Objectives

This project demonstrates practical experience with:

- DevSecOps
- Shift-Left Security
- CI/CD Security Automation
- Container Security
- Vulnerability Management
- Kubernetes Deployments
- Infrastructure as Code