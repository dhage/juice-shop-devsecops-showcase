# DevSecOps Showcase with OWASP Juice Shop

![Dependency Check](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/dependency-check.yaml/badge.svg)
![SAST Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/sast.yaml/badge.svg)
![Container Security Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/trivy.yaml/badge.svg)
![Security Gate](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/security-gate.yaml/badge.svg)
![Kubernetes Security Scan](https://github.com/dhage/juice-shop-devsecops-showcase/actions/workflows/checkov.yaml/badge.svg)

## Overview

This project demonstrates a practical end-to-end DevSecOps implementation using OWASP Juice Shop.

The objective is to integrate automated security controls throughout the software delivery lifecycle by combining CI/CD automation, security scanning, container security, Infrastructure as Code, and Kubernetes deployment.

---

## Project Status

This project is actively developed as a hands-on DevSecOps showcase demonstrating secure software delivery practices, automated security testing and infrastructure security validation.

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
 ├─ Trivy (Container Security)
 └─ Checkov (Kubernetes Security)
    ↓
Security Gate
    ↓
Docker Image
    ↓
Kubernetes Deployment
    ↓
Monitoring
 ├─ Prometheus
 └─ Grafana
    ↓
Governance & Documentation
 ├─ Threat Model
 ├─ Risk Assessment
 ├─ Security Controls
 └─ ADRs
```

---
## Technologies

| Area | Technology |
|--------|------------|
| Application | OWASP Juice Shop |
| Containerization | Docker |
| CI/CD | GitHub Actions |
| SAST | Semgrep |
| Software Composition Analysis | OWASP Dependency Check |
| Container Security | Trivy |
| Kubernetes Security | Checkov |
| Container Orchestration | Kubernetes |
| Infrastructure as Code | Terraform |
| Security Governance | Security Gate |
| Monitoring | Prometheus, Grafana |

---

## Local Setup

### Start Application

```bash
docker compose up -d
```

Application URL:

[http://localhost:3000](http://localhost:3000)

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
  - Detection of HIGH and CRITICAL vulnerabilities
  - Automated security checks during CI/CD execution
  - Findings documented in [Trivy Findings Report](reports/trivy-findings.md)

### Kubernetes Security

- Checkov
  - Kubernetes manifest analysis
  - Infrastructure security validation
  - Security misconfiguration detection
  - Findings documented in [Checkov Findings Report](reports/checkov-findings.md)

---

## Security Governance

A dedicated Security Gate validates the results of all automated security scans before deployment activities can proceed.

### Security Validations

- Semgrep SAST validation
- OWASP Dependency Check validation
- Trivy container vulnerability validation
- Checkov Kubernetes security validation

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

## Terraform Infrastructure

Infrastructure as Code resources are located in the `terraform` directory.

### Components

- Provider Configuration
- Variables
- Security Group Definition
- Outputs

Example:

```bash
terraform init
terraform validate
terraform plan
```

---

## Secure SDLC

This project demonstrates how security can be integrated into every phase of the software development lifecycle through automated testing, infrastructure validation, governance controls and continuous security monitoring.

### Implemented Practices

- Shift-Left Security
- Static Application Security Testing (SAST)
- Software Composition Analysis (SCA)
- Container Security Scanning
- Kubernetes Security Validation
- Security Governance
- Threat Modeling
- Risk Assessment
- Architecture Decision Records (ADRs)

### Architecture Decision Records

The project documents important architectural and security decisions using ADRs.

Current ADRs:

- ADR-001: Static Application Security Testing with Semgrep
- ADR-002: Container Security Scanning with Trivy
- ADR-003: Kubernetes Security Validation with Checkov
- ADR-004: Security Gate Implementation

---

## Repository Structure

```text
.
├── .github/workflows
│   ├── sast.yaml
│   ├── trivy.yaml
│   ├── dependency-check.yaml
│   ├── security-gate.yaml
│   └── checkov.yaml
│
├── docs
│   ├── secure-sdlc.md
│   └── architecture-decisions
│       ├── ADR-001-semgrep.md
│       ├── ADR-002-trivy.md
│       ├── ADR-003-checkov.md
│       └── ADR-004-security-gate.md
│
├── kubernetes
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   └── README.md
│
├── monitoring
│   ├── prometheus.yaml
│   └── grafana
│       └── README.md
│
├── terraform
│   ├── provider.tf
│   ├── variables.tf
│   ├── main.tf
│   ├── outputs.tf
│   └── README.md
│
├── reports
│
├── security
│   ├── threat-model.md
│   ├── risk-assessment.md
│   └── security-controls.md
│
└── README.md
```

---

## Roadmap

- [x] Dockerized OWASP Juice Shop
- [x] GitHub Actions CI/CD
- [x] Semgrep SAST
- [x] Trivy Container Scanning
- [x] OWASP Dependency Check
- [x] Security Gate Implementation
- [x] Kubernetes Manifests
- [x] Terraform Infrastructure
- [x] Kubernetes Security Scanning
- [x] Security Documentation
- [x] Threat Modeling
- [x] Risk Assessment
- [x] Secure SDLC
- [x] Architecture Decision Records (ADR)
- [x] Prometheus Configuration
- [x] Grafana Dashboard Planning

---

## Security Documentation

Security documentation is maintained within the `security` directory.

### Available Documents

- Threat Model
- Risk Assessment
- Security Controls Catalog
- Secure SDLC
- Architecture Decision Records (ADR)

### Documentation

- [Threat Model](security/threat-model.md)
- [Risk Assessment](security/risk-assessment.md)
- [Security Controls](security/security-controls.md)
- [Secure SDLC](docs/secure-sdlc.md)

---

## What This Project Demonstrates

This repository demonstrates practical implementation of:

- Secure CI/CD Pipelines
- Shift-Left Security
- Security Automation
- Security Governance
- Infrastructure as Code
- Kubernetes Security
- Threat Modeling
- Security Documentation

---

## Learning Objectives

This project demonstrates practical experience with:

- DevSecOps
- Shift-Left Security
- CI/CD Security Automation
- Security Governance
- Vulnerability Management
- Software Composition Analysis (SCA)
- Container Security
- Kubernetes Deployments
- Infrastructure as Code
- GitHub Actions Workflows
- Threat Modeling
- Risk Assessment
- Secure Software Development Lifecycle (SSDLC)
- Architecture Decision Records (ADR)